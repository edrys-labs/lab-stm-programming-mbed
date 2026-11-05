# lab-stm-programming-mbed

HelloWorld Lab in C and C++ (STM HAL, mbed) ...

![screenshot](./media/demo.png)

In order to run this lab, you will need docker on the computer that is running in station mode.
The image with the pyxtermjs server and the tools to program the STM32 board is built from the Dockerfile in [lab-stm32](https://github.com/edrys-labs/lab-stm32), once:

```bash
git clone https://github.com/edrys-labs/lab-stm32
docker build -t edrys-stm-lab lab-stm32
```

Then start it:

``` bash
docker run -it --privileged \
    --name edrys_arm_development \
    -p 127.0.0.1:5000:5000 \
    -e PYXTERM_CMD=zsh \
    --device /dev/ttyACM0 \
    -v /media/$USER/DIS_L4IOT:/media/appuser/DIS_L4IOT \
    -v /dev/disk/by-id:/dev/disk/by-id \
    -v /dev/serial/by-id:/dev/serial/by-id \
    -v /run/udev:/run/udev:ro \
    edrys-stm-lab
```

As an alternative, you can also run the terminal server manually from your machine by using Python.
For more information on this, please visit:

https://github.com/edrys-labs/module-pyxtermjs

## Lab Configuration

There are two ways to deploy this lab, using the `Deploy` button:

[<img src="https://img.shields.io/badge/%F0%9F%9A%80%20-%20Deploy%20Lab%20-%20light?style=plastic" height="25" />](https://edrys-labs.github.io/?/deploy/https://raw.githubusercontent.com/edrys-labs/lab-stm-programming-mbed/main/laboratory/base.yaml)

Or, if you already have created a new classroom for [edrys-Lite](https://edrys-labs.github.io), you can add this lab to your classroom by importing the following URL:

https://raw.githubusercontent.com/edrys-labs/lab-stm-programming-mbed/main/laboratory/base.yaml

## Demo

https://github.com/edrys-labs/lab-stm-programming-mbed/assets/3089101/59ef0e89-dbab-4d64-a1d8-933c34f841a6
