# Drone Gate 

## How to use warehose with the drone gates

You need to clone the gazebo models from px4 and the drone gate repository

>cd $HOME
>
>git clone https://github.com/PX4/PX4-SITL_gazebo.git
>
>git clone https://github.com/pedrogasg/drone-gate.git drone_gate

If the GAZEBO_MODEL_PATH is defined

>export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:$HOME/PX4-STIL_gazebo/models:$HOME/drone_gate/models

and if is not defined

>export GAZEBO_MODEL_PATH=$HOME/PX4-SITL_gazebo/models:$HOME/drone_gate/models

once the models are in the path you can use the world warehouse 

> gazebo drone_gate/worlds/warehouse.world

or add more gates
```xml
    <include>
      <name>drone_gate</name>
      <uri>model://drone_gate</uri>
      <pose>0 0 0 0 0 0</pose>
    </include>
```