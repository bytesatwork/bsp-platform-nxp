# bytesatwork BSP platform manifest for IMX8MM/IMX8MP/IMX93 based modules

This repository contains the manifest for [repo](https://source.android.com/setup/develop/repo) and is intended to
simplify the build procedure for the following devkits by [bytesatwork](https://www.bytesatwork.io):

- byteDEVKIT IMX8MM
- byteDEVKIT IMX8MP
- byteDEVKIT IMX93


## Usage

Use repo to download all necessary repositories:

	repo init -u https://github.com/bytesatwork/bsp-platform-nxp.git -b scarthgap
	repo sync

When these commands are completed successfully, the following command will setup a
Yocto Project environment:

### byteDEVKIT IMX8MM

```
MACHINE=bytedevkit-imx8mm DISTRO=poky-bytesatwork EULA=1 . setup-environment build
```

### byteDEVKIT IMX8MP

```
MACHINE=bytedevkit-imx8mp DISTRO=poky-bytesatwork EULA=1 . setup-environment build
```

### byteDEVKIT IMX93

```
MACHINE=bytedevkit-imx93 DISTRO=poky-bytesatwork EULA=1 . setup-environment build
```

The final command builds a minimal image:

	bitbake bytesatwork-minimal-image

The output is found in:

### byteDEVKIT IMX8MM

```
tmp/deploy/images/bytedevkit-imx8mm
```

### byteDEVKIT IMX8MP

```
tmp/deploy/images/bytedevkit-imx8mp
```

### byteDEVKIT IMX93

```
tmp/deploy/images/bytedevkit-imx93
```


## Note
The software provided is optimized for development convenience and is not suitable for use in production.


## Support

Refer to our [byteWIKI](https://bytewiki.readthedocs.io/en/latest/softwaredevelopment.html) for comprehensive information and guidance on software development.

If you have any questions or encounter any issues while using our products or services, please don’t hesitate to reach out to our support team.

Please feel free to contact us at support@bytesatwork.ch for any questions, comments or pull requests.

We are here to help and will get back to you as soon as possible.
