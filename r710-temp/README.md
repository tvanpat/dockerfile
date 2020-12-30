# r710-auto-fan

A bash script to control the fan speed of an R710 based upon current ambeint tempature.

Creates a container that will monitor the R710 tempature using IPMI through the idrac module.

If the current tempature is above the max tempature manual fan control will be disabled and the server will attempt to cool itself using its own fan settings.  This can be very loud.  Below the max temp the script will enable manual fan control and will adjust to fan speeds to keep the server cool while attempting to keep fan noise minimal.

There are three enviromental variables which need to be set:

- IPMIHOST: This is the IP address of you Idrac controller

- IPMIUSER: This is the user name on your idrac controller, the default is root

- IPMIPW: This is the password on your idrac controller, the default is calvin.

This container/script was built heavily off the R710-IPMI-TEMP script located on [GitHub](https://github.com/NoLooseEnds/Scripts/tree/master/R710-IPMI-TEMP)