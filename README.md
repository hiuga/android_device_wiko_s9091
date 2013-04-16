android_device_wiko_s9091
=========================


initialize repo with cm9 repository:
	
	repo init -u git://github.com/CyanogenMod/android.git -b ics

Now retrieve Wiko PEAX repositories (Should be using local_manifests.xml instead):

	mkdir -p .repo/local_manifests
	wget https://github.com/wiko-repo/android_device_wiko_common/raw/ics/manifests/local_manifest.xml -O .repo/local_manifests/local_manifest.xml
	wget https://github.com/wiko-repo/android_device_wiko_s9091/raw/ics/s9091_manifest.xml -O .repo/local_manifests/s9091_manifest.xml

Now prepare to build

	. build/envsetup.sh
	brunch s9091

And there we are :). Now debugging time ...
