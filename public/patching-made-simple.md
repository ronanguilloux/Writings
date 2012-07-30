Patching made simple
====================

Summary
------- 

* Create old/, new/ and patched/ directories, where patched/ is an exact copy of old/
* Create a patch to be applied to patched/
* Patch patched/
* Test patched/

Step-by-step procedure
----------------------

For this example, the old version is a zipped release & the new one is git-based:

    cd /tmp

(=> move the myOldSources.zip inside /tmp)

old :

    unzip myOldSources.zip

    mv myOldSources old

new :

    git clone git@myServer:repositories/Project.git

    mv Project new

remove git files

    rm old/.git -rf

    rm new/.git -rf

    rm new/.gitignore

    rm old/.gitignore

create a patch

    cp old patched -r

    diff -urN --binary old new > patched/YEAR-Month-Day.patch

OR alternatively, for quick check, avoid EOL differences adding -w option : 

    diff -wurN --binary old new > patched/YEAR-Month-Day.patch)

check patch 

    cd patched

    view YEAR-Month-Day.patch

try patch

    patch --dry-run --no-backup-if-mismatch -u -p1 < YEAR-Month-Day.patch

OR alternatively, use --binary : 

    patch --dry-run --binary --no-backup-if-mismatch -u -p1 < YEAR-Month-Day.patch

if ok, apply patch

    patch --no-backup-if-mismatch -u -p1 < YEAR-Month-Day.patch
