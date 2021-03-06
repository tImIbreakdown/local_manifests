# Lineage buildscripts
========================

Please note, I use ~/android/lineage in this README but you can use whatever folder name you want.

Also please note that repopick.sh isn't always updated. Please check LineageOS Gerrit in case there is changes to repopick topics.

Starting from zero:
---------
    mkdir -p ~/android/lineage
    cd ~/android/lineage
    repo init -u git://github.com/LineageOS/android.git -b lineage-17.0
    mkdir -p .repo/local_manifests
    curl https://raw.githubusercontent.com/tImIbreakdown/local_manifests/lineage-17.0/local_manifest.xml > .repo/local_manifests/my_manifest.xml
    repo sync
    # OPTIONAL to use repopick unless you want to test WIP commits
    curl https://raw.githubusercontent.com/lineage-o-x2/local_manifests/lineage-16.0/repopick.sh > repopick.sh
    . repopick.sh

If you've already synced Lineage-Sources:
----------
    mkdir -p .repo/local_manifests
    curl https://raw.githubusercontent.com/tImIbreakdown/local_manifests/lineage-17.0/local_manifest.xml > .repo/local_manifests/my_manifest.xml
    repo sync
    # OPTIONAL to use repopick unless you want to test WIP commits
    curl https://raw.githubusercontent.com/lineage-o-x2/local_manifests/lineage-16.0/repopick.sh > repopick.sh
    . repopick.sh

Building
----------
    cd ~/android/lineage
    curl https://raw.githubusercontent.com/tImIbreakdown/local_manifests/lineage-17.0/clean.sh > clean.sh
    curl https://raw.githubusercontent.com/tImIbreakdown/local_manifests/lineage-17.0/dirty.sh > dirty.sh
    . clean.sh // for clean builds
    . dirty.sh // for dirty builds

I made these modified scripts for convenience plus logs terminal output to files for easy scrolling later in your favorite text editor.
