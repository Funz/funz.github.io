---
title: "Simulation on local network or cloud subnet"
permalink: /docs/sim_net/
---

An efficient way to launch many simulation is to use other local network computers, while using your own computer to launch Funz commands. 

Assuming that the simulation software (say Modelica, our standard example) is already installed on the other local network computers, on each you just have to:

  * intall Funz: 
    * Python: `pip install Funz`, then `import Funz`
    * R: `remotes::install_github('Funz/Funz.R')`, then `library(Funz)`
    * bash/cmd.exe: download and unzip [Funz-Bash.zip](https://github.com/Funz/plugin-Bash/releases/latest) or [Funz-Cmd.exe.zip](https://github.com/Funz/plugin-Cmd.exe/releases/latest)
  * install simulation plugin:
    * Python: `Funz.installModel('Modelica')`
    * R: `Funz::install.Model('Modelica')`
    * bash/cmd.exe: download and unzip [plugin-Modelica.zip](https://github.com/Funz/plugin-Modelica/releases/latest)
  * if needed, setup simulation script 'Funz/scripts/Modelica.sh' or 'Funz/scripts/Modelica.bat'
  * __add your own computer IP (say 192.168.1.123) in the 'Funz/calculator.xml' file:__
    ```
    <CALCULATOR>
    ...
    <HOST name="192.168.1.123" port="19001">
    <HOST name="192.168.1.123" port="19002">
    <HOST name="192.168.1.123" port="19003">
    <HOST name="192.168.1.123" port="19004">
    ...
    </CALCULATOR>
    ```
  * start background Funz computing daemon:
    * Python: `Funz.startCalculators(1)`
    * R: `Funz::startCalculators(1)`
    * bash/cmd.exe: launch backend `Funz/FunzDaemon.sh` or `Funz/FunzDaemon.bat`

  ---

  You can now check that these computers are well setup by running basic example on your own, that will use one of the local network computers:

  *  check that you well receive network Funz heartbeats: `nc -lu 19001` or `socat -u udp-recv:19001`
  *  launch basic calculation:
    * Python: `Funz.Run(model="Modelica",input_files="samples/NewtonCooling.mo")`
    * R: `Funz::Run(model="Modelica",input.files="samples/NewtonCooling.mo")`
    * bash/cmd.exe: `./Funz.sh Run -m Modelica -if samples/NewtonCooling.mo` or `./Funz.bat Run -m Modelica -if samples/NewtonCooling.mo` 
