# Xiaomi Redmi 7 / Redmi Y3 (onclite)

Inline device tree source for msm-4.9, SDM632 + PMI632. Based on CAF tag
`LA.UM.8.6.2.r1-04900-89xx.0` (`onc-q-oss`).

Copy `onclite.dts` and `onclite/` into `arch/arm64/boot/dts/qcom/`, add the target to
the Makefile and enable it in the defconfig. `CONFIG_BUILD_ARM64_DT_OVERLAY=y` is
required, the bootloader applies an overlay from the `dtbo` partition onto the base
dtb and that needs the `__symbols__` node.

`ARM64: dts: qcom: Add overlayed onclite dtsi`
https://github.com/crsvt/android_kernel_xiaomi_onclite/commit/84d80e7d09e94e75aee9c19e7b47a240314d377f
