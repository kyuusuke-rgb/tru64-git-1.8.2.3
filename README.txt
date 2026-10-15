===================================================================

 Git 1.8.2.3 for Tru64 UNIX (OSF/1 5.1b) - Binary Package

 Target: alphaev56-dec-osf5.1b

===================================================================



1. DESCRIPTION

   This package contains Git 1.8.2.3 built natively on Tru64 UNIX v5.1b.

   It includes required runtime shared libraries (libz, libintl, 

   libiconv, and libgcc_s) for immediate standalone deployment.



2. CONTENTS

   - /usr/local/bin/git*

   - /usr/local/libexec/git-core

   - /usr/local/share/git-core

   - /usr/local/lib/libz.so*

   - /usr/local/lib/libintl.so*

   - /usr/local/gcc474/lib/libiconv.so*

   - /usr/local/gcc474/lib/libgcc_s.so*



3. EXTRACT / RESTORE

   Run the following commands as root to extract to / :



     cd /

     gzip -d -c /usr/local/src/Tru64_Git_1.8.2.3_full.tar.gz | tar xvf -



4. ENVIRONMENT SETUP (.profile or .bashrc)

   Add the following lines to your user shell environment:



     export PATH=/usr/local/bin:$PATH

     export LD_LIBRARY_PATH=/usr/local/lib:/usr/local/gcc474/lib:$LD_LIBRARY_PATH



5. VERIFICATION

   Test the installation and dynamic linker using:



     git --version

     ldd /usr/local/bin/git



   Expected output: "git version 1.8.2.3"

   (Ensure no "not found" libraries appear in ldd output)

===================================================================
