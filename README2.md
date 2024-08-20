## Troubleshooting

### error reading format of config

The system was set with it_IT.UTF-8 and not en_US.UTF-8 so he read string and not double in numeber formats

### problem with connecting with the sensor

You can have the data using the witmotion-uart-qt code in sudo but not under mini user even if he was under the dialout user group. removing the modemmanager package seems to have solve this issue, need more test

### not reading the data from the yaml

The data was not readed becouse in the launch file, in the node launch, the variable name='witmotion_ros' was not set. this cause to launch the node maybe with a different name that was not found in the yaml description and so that parameters was not readed