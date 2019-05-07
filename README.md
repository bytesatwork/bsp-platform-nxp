# bytes at work AG BSP platform manifest for IMX8MM based modules

This repository contains the manifest for [repo](https://source.android.com/setup/develop/repo) and is intended to
simplify the build procedure for byteDEVKIT IMX8MM by [bytes at work AG](https://www.bytesatwork.io).

## Usage

Use repo to download all necessary repositories:

	repo init -u https://github.com/bytesatwork/bsp-platform-nxp.git -b dunfell
	repo sync

When these commands are completed successfully, the following command will setup a
Yocto Project environment for byteDEVKIT IMX8MM:

	MACHINE=bytedevkit-imx8mm DISTRO=poky-bytesatwork EULA=1 . setup-environment build

The final command builds a minimal image:

	bitbake bytesatwork-minimal-image

The output is found in:

	tmp/deploy/images/bytedevkit-imx8mm
