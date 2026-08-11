# LOQ Plymouth sample

**Clone the repo then**

## Install

```bash
sudo mkdir -p /usr/share/plymouth/themes/custom-loq
sudo cp -r loq.plymouth loq.script frames /usr/share/plymouth/themes/custom-loq/
```

## Register (Once)

```bash
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/custom-loq/loq.plymouth 100
```

## Select (If not selected)

```bash
sudo update-alternatives --config default.plymouth
```

## Rebuild

```bash
sudo update-initramfs -u
```

The animation uses the PNG files in the frames directory, named `frame_0.png`, `frame_1.png`, `frame_2.png`, and so on. The script will cycle through them in order.

## For update

```bash
sudo rm -rf /usr/share/plymouth/themes/custom-loq/*
sudo cp -r loq.plymouth loq.script frames /usr/share/plymouth/themes/custom-loq/
sudo update-alternatives --config default.plymouth
```

