# RedCare Pharmacy Automation

## Run the following command to install Maestro on Mac OS, Linux or Windows (WSL):

```shell
curl -Ls "https://get.maestro.mobile.dev" | bash
```

## Installing a specific version of Maestro

```shell
ENV MAESTRO_VERSION {version}
```

## Connecting to Device

### Android

maestro test will automatically detect and use any local emulator or USB-connected physical device.

## Specify a Device(Optional- only needed if multiple simulators and emualtors are open)

### Android
To list your running Android devices, run the following command in your terminal:

```shell
adb devices
```
```shell
maestro --device <device Id> test tests/flows.yaml
```

## Run tests

If the tests contain external parameters(These tests contain external parameters like Username, Password and SearchInput)

```bash
maestro test -e env=debug -e Username=user -e Password=password123 -e SearchInput=IBUPROFEN tests/flows.yaml
```
(env,password,Username and searchtext is an example. Please use your credentials,env and the text to be searched)

If the tests do not have parameters.

```bash
maestro test tests/flows.yaml
```

## Links 

- [Maestro Docs](https://maestro.mobile.dev/) 

