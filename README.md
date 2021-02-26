# Build instructions
Follow the instructions from Google to setup a machine to build AOSP:
https://source.android.com/setup/build/initializing

Then, sync all the sources:
```
$ repo init -u https://android.googlesource.com/platform/manifest -b master
$ cd .repo
$ git clone https://github.com/trautamaki/local_manifests.git local_manifests
$ cd ..
$ repo sync -c --no-clone-bundle --no-tags
```
then:
```
$ source build/envsetup.sh
$ lunch aosp_cheeseburger-user
$ make otapackage -j12
```
