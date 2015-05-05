reach-platform
==============

Install the `repo` utility:

$: mkdir ~/bin  
$: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo  
$: chmod a+x ~/bin/repo  

Download the BSP source:

$: PATH=${PATH}:~/bin  
$: mkdir reach-bsp  
$: cd reach-bsp  
$: repo init -u https://github.com/jmore-reachtech/reach-platform -b dizzy 
$: repo sync  

Once this has completed, you will have all you need. To start a build:

$: DISTRO=reach MACHINE=g2h-solo-4 source ./setup-environment build  
$: bitbake reach-image-minimal
(and grab a few coffees)
