# Anoubis
Python 3.9 or newer(in %PATH% for Windows).
ADB (in %PATH% for Windows).
The CVE-2020-0069 PoC (Anoubis).
Based on https://github.com/R0rt1z2/AutomatedRoot
Available options
Root the device. (system-mode + SuperSU).
Root the device. (bootless-mode + Magisk).
Unroot the device. (supports both bootless and system mode).

Make sure you meet all the requirements listed above, especially the first and last ones.

Download the current Anoubis zip file to your PC and unzip it. Inside will be 2 directories: 'arm' & 'arm64' with an 'Anoubis' binary in each. Pick one for 
your device. Differences between the flavors:

arm64: 64-bit kernel and userspace

arm: 32-bit userspace on a 64-bit or 32-bit kernel (will also work in 64-bit userspace)

Connect your device to ADB and push Anoubis to your /data/local/tmp folder

adb push path/to/Anoubis /data/local/tmp/

Open an adb shell

adb shell

Change to your tmp directory

cd  /data/local/tmp

Add executable permissions to the binary

chmod 755 Anoubis

At this point keep your device screen on and don't let it go to sleep. Run the command

./Anoubis

It should only take a second or two. If the program gets stuck for more than a few seconds and your device is awake, press Ctrl+C to close it.

The -v option turns on verbose printing, which is necessary for me to debug any problems.

The output of ./Anoubis -v is similar to this:

