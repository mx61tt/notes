# Android Studio on Kali

## 1. Downloading Android Studio from official website

{% embed url="https://developer.android.com/studio" %}

## 2. Adding the 32-bit architecture for install prerequisites

```shell
sudo dpkg --add-architecture i386
```

## 3. Installing prerequisites

```shell
sudo apt update
sudo apt install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
```

## &#x20;4. Decompressing files

```shell
sudo tar -xf ~/Downloads/android-studio-2021.3.1.17-linux.tar.gz -C /opt
```

## 5. Starting Android Studio

```shell
sudo /opt/android-studio/bin/studio.sh
```
