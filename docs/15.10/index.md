---
tocdepth: 3
---

(ubuntu-15-10-release-notes)=
# Ubuntu 15.10 "Wily Werewolf" Release Notes

<!-- Source: https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes -->

## When adding features to this page, please add credits for the relevant upstream developers where appropriate.
||<tablestyle="float:right; width:40%; background:#F1F1ED; margin: 0 0 1em 1em;" style="padding:0.5em;">'''Table of Contents'''<<BR>> <<TableOfContents(2)>>||

= Introduction =

These release notes for '''Ubuntu 15.10''' (Wily Werewolf) provide an overview of the release and document the known issues with Ubuntu 15.10 and its flavors.

=== Support lifespan ===
Ubuntu 15.10 will be supported for 9 months for Ubuntu Desktop, Ubuntu Server, Ubuntu Core, Kubuntu, Ubuntu Kylin along with all other flavours.

=== Official flavour release notes ===
Find the links to release notes for official flavors [[#Official_flavours|here]].

<<BR>>
= Get Ubuntu 15.10 =
== Download Ubuntu 15.10 ==

Images can be downloaded from a location near you.
## <<BR>>'''Note:''' The Ubuntu Desktop images are now bigger than a standard CD, and you should use a USB or DVD for installation.

You can download ISOs from:

http://releases.ubuntu.com/15.10/ (Ubuntu Desktop, Server, and Snappy Core) <<BR>>
http://cdimage.ubuntu.com/ubuntu/releases/15.10/release/ (Less Popular Ubuntu Images) <<BR>>
http://cloud-images.ubuntu.com/releases/15.10/release/ (Ubuntu Cloud Server) <<BR>>
http://cdimage.ubuntu.com/netboot/15.10/ (Ubuntu Netboot) <<BR>>
## branding of this is still under discussion and we shouldn't highlight these images in the release notes
##http://cdimage.ubuntu.com/ubuntu-core/releases/15.10/release/release/ (Ubuntu Core) <<BR>>
##http://cdimage.ubuntu.com/edubuntu/releases/15.10/release/release/ (Edubuntu DVD) <<BR>>
http://cdimage.ubuntu.com/kubuntu/releases/15.10/release/ (Kubuntu) <<BR>>
http://cdimage.ubuntu.com/lubuntu/releases/15.10/release/ (Lubuntu) <<BR>>
http://cdimage.ubuntu.com/ubuntustudio/releases/15.10/release/ (Ubuntu Studio) <<BR>>
http://cdimage.ubuntu.com/ubuntu-gnome/releases/15.10/release/ (Ubuntu GNOME) <<BR>>
http://cdimage.ubuntu.com/ubuntukylin/releases/15.10/release/ (Ubuntu Kylin) <<BR>>
http://cdimage.ubuntu.com/ubuntu-mate/releases/15.10/release/ (Ubuntu MATE) <<BR>>
http://cdimage.ubuntu.com/xubuntu/releases/15.10/release/ (Xubuntu) <<BR>>
##http://cdimage.ubuntu.com/mythbuntu/releases/15.10/release/ (Mythbuntu) <<BR>>
##http://cdimage.ubuntu.com/kubuntu-active/releases/15.10/release/ (Kubuntu Active) <<BR>>

##To install Ubuntu 15.04 for phones, follow the instructions found at [[Touch/Install]] to download and flash an image to your device.

== Upgrading from Ubuntu 15.04 ==

To upgrade on a desktop system:
 * Open the "Software & Updates" Setting in System Settings.
 * Select the 3rd Tab called "Updates".
 * Set the "Notify me of a new Ubuntu version" dropdown menu to "For any new version".
 * Press Alt+F2 and type in "update-manager" (without the quotes) into the command box.
 * Update Manager should open up and tell you: New distribution release '15.10' is available.
 * Click Upgrade and follow the on-screen instructions.

To upgrade on a server system:
 * Install the {{{update-manager-core}}} package if it is not already installed.
 * Make sure the /etc/update-manager/release-upgrades is set to normal.
 * Launch the upgrade tool with the command {{{sudo do-release-upgrade}}}.
 * Follow the on-screen instructions.
Note that the server upgrade will use GNU screen and automatically re-attach in case of dropped connection problems.

There are no offline upgrade options for Ubuntu Desktop and Ubuntu Server. Please ensure you have network connectivity to one of the official mirrors or to a locally accessible mirror and follow the instructions above.

<<BR>>
= New features in 15.10 =

## Please see the [[https://blueprints.launchpad.net/ubuntu/wily/+specs|Wily blueprint list]] for details.

== Updated Packages ==

As with every new release, packages--applications and software of all kinds--are being updated at a rapid pace. Many of these packages came from an automatic sync from [[http://www.debian.org|Debian]]'s unstable branch; others have been explicitly pulled in for Ubuntu 15.10.

For a list of all packages being accepted for Ubuntu 15.10, please subscribe to [[https://lists.ubuntu.com/mailman/listinfo/wily-changes|wily-changes]].

== Linux kernel 4.2 ==

Linux 4.2 is another exciting update with the following highlights:

  * New AMDGPU kernel driver for supporting recent and near-term Radeon GPUs
  * Intel Broxton support
  * F2FS file-system encryption support
  * NV-DIMM support

A new kernel for the Raspberry Pi 2 has also landed in the official archive.

##== Boot and service management ==
##
##[[http://freedesktop.org/wiki/Software/systemd/|systemd]] integration has been improved. 

== Ubuntu Desktop ==

The general theme for 15.10 on the desktop is one of bug fixes and incremental quality improvements as well as a more significant change in the move to systemd as an init system.

=== Unity ===

Unity has had many bugs fixed and new features added.  Locally integrated menus are now available for unfocussed windows.  There have been a number of usability improvements to the dash.

=== Compiz ===

 *  Various fixes and improvements.
 *  Refined integration with the MATE desktop.

=== General ===

 * Firefox is updated to version 41 and Chromium is updated to version 45.
 * MATE is updated to 1.10.
 * Most of the GNOME platform is now based on version 3.16.
 * Blueman 2.0 is now included and used by several flavours along with BlueZ 5.35.
 * Support for the new Steam Controller - Just install Steam from the Software Center and then pair the controller in Big Picture mode. 

=== LibreOffice ===

LibreOffice 5.0.2 brings a lot of improvements to entire package.  For more information on these improvements please see the !LibreOffice release notes [[https://wiki.documentfoundation.org/ReleaseNotes/5.0|available here]].

##=== Ubuntu Make (nee Developer Tools Centre) ===
##
##Ubuntu Make continues to add support for new platforms, bringing the total to 15 (from 1 last release).  This includes highlights such as:
##
## * Android NDK support and bumped Android Studio to latest version
## * Other new IDEs: IDEA (ultimate and community editions), pycharm (professional, educational and community ##editions), webstorm, rubymine, phpstorm and eclipse
## * Golang compiler support
## * Firefox developer edition
## * Dartlang editor
## * Stencyl game development platform
## * Numerous usability improvements and accessibility (ppa, doc)
##
##These new features are also available to LTS users.
##
##We also rationalized 3rd party library managers so that they all behave the same and don't overwrite and/or ##mix with system libraries. Developers don't have to worry about messing up up their installation if they want to install PyPI, npm, rubygem libraries.
##

== Ubuntu Server ==

=== OpenStack Liberty ===

Ubuntu 15.10 includes  the latest !OpenStack release, Liberty, including the following components:

 * !OpenStack Identity - Keystone
 * !OpenStack Imaging - Glance
 * !OpenStack Block Storage - Cinder
 * !OpenStack Networking - Neutron
 * !OpenStack Telemetry - Ceilometer and Aodh
 * !OpenStack Orchestration - Heat
 * !OpenStack Dashboard - Horizon
 * !OpenStack Object Storage - Swift
 * !OpenStack Database as a Service - Trove
 * !OpenStack DNS - Designate
 * !OpenStack Bare-metal - Ironic
 * !OpenStack Filesystem - Manila
 * !OpenStack Key Manager - Barbican

Ubuntu 15.10 provides Swift 2.5.0 including experimental support for erasure coded storage.

Please refer to the [[https://wiki.openstack.org/wiki/ReleaseNotes/Liberty|OpenStack Liberty release notes]] for full details of this release of !OpenStack.

!OpenStack Liberty is also provided via the [[ServerTeam/CloudArchive|Ubuntu Cloud Archive]] for !OpenStack Liberty for Ubuntu 14.04 LTS users.

Ubuntu 15.10 also includes the second Ubuntu release of of the Nova driver for LXD ('nova-compute-lxd'). This driver should not be considered ready for production use and is still provided for experimentation and early testing at this point in time in preparation for its first GA release in 16.04.

'''WARNING''': Upgrading an !OpenStack deployment is a non-trivial process and care should be taken to plan and test upgrade procedures which will be specific to each !OpenStack deployment.

Make sure you read the [[https://wiki.ubuntu.com/ServerTeam/OpenStackCharms/ReleaseNotes1510|OpenStack Charm Release Notes]] for more information about how to deploy Ubuntu !OpenStack using Juju.

=== Juju ===

Juju, the service orchestration tool for Ubuntu, has been updated to the latest current stable release, 1.24.6. See the upstream [[https://juju.ubuntu.com/docs/reference-release-notes.html|release notes]] for full details of all new features and improvements in this release.

=== libvirt 1.2.16 ===

Libvirt has been updated to the 1.2.16 release.

=== qemu 2.3 ===

Qemu has been updated to the 2.3 release.

See http://wiki.qemu.org/ChangeLog/2.3 for details.

=== Open vSwitch 2.4.0 ===

Ubuntu 15.10 includes the latest release of Open vSwitch, 2.4.0.

Ubuntu 15.10 also includes an experimental preview of Open vSwitch integrated with DPDK (Data Plane Development Kit) enabling fast packet processing through userspace usage of compatible networking cards - see the openvswitch-switch-dpdk package for more details.

=== Ceph 0.94.3 ===

Ubuntu 15.10 includes the latests stable release of Ceph, 0.94.3 'Hammer'.

For full details on the Ceph Hammer release, please refer to the [[http://ceph.com/docs/master/release-notes/|upstream release notes]].

##=== LXC ===
##
##The LXC container manager was updated to the latest upstream version, 1.1. More specifically the 1.1.2 bugfix release. This brings full systemd support, both on the host and in the container as well as new features such as checkpoint/restore using CRIU, openvswitch support and support for qcow2 backed containers.
##
##More details on the new LXC release can be found at: https://linuxcontainers.org/lxc/news/
##
##This new version of LXC also comes with a new helper filesystem called LXCFS. That filesystem exposes the ##container resource limits into the container so that tools like free, top, ... report them properly. It's ##also a vital part of making Systemd work properly in containers.
##
##More details on the new LXCFS release can be found at: https://linuxcontainers.org/lxcfs/news/
##
##CGManager, the LXC CGroup manager was also updated to version 0.36, fixing many bugs and introducing some new features that were needed for LXCFS.
##
##More details on the new CGManager release can be found at: https://linuxcontainers.org/cgmanager/news/
##
##=== LXD ===
##
##Ubuntu 15.10 is the first Ubuntu release to feature LXD.
##
##LXD has been developped to provide a fast, reliable and scalable way to manage system containers across the ##network.
##It's entirely image based, secure by default, supports snapshots, live migration and offers a simple yet ##powerful REST API.
##
##LXD ships with two clients:
## - lxc, a command line client for small and medium size deployments where the operator doesn't mind or ##prefers manual control.
## - nova-compute-lxd, an OpenStack Nova plugin which makes managing containers as simple as managing virtual ##machines.
##
##Ubuntu 15.10 ships with LXD 0.7. This is the result of an intense 6 months of development and while not ready for production workloads, it's definitely ready for experimentation.
##
##More details on LXD can be found at: https://linuxcontainers.org/lxd##
##=== MAAS ===
##
##MySQL has been updated to 5.6 and remains in main. In universe, Percona XtraDB Cluster has been updated to ##5.6, MariaDB to 10.0 and Percona Server 5.6 has been added.
##
##With the switch to systemd, process limits such as the maximum number of open files can now be controlled by tuning the unit configuration file, and MySQL and variant daemons are already limited by systemd defaults. If you are already tuning these values, we recommend that you remove any open_files_limit type configuration settings from my.cnf and configure everything from the systemd unit file instead in order to avoid conflicts between configurations in both locations. See [[https://launchpad.net/bugs/1434758|bug 1434758]] for details.
##=== cloud-init 0.7.7 ===
##
##Cloud-init now uses Python 3, and uses systemd.  It supports running on Digital Ocean and base64 encoded ##user-data on Google Compute.  Chef support is also improved.
##
##=== docker 1.5.0 ===
##
##The release notes describing the features available in docker 1.5 are located here: https://docs.docker.
##com/v1.5/release-notes/
##
##In addition to the features outlined above, we have provided experimental support for ppc64el and arm64.
##
##=== HA related package updates ===
## * corosync 2.3.4
## * haproxy 1.5.0
## * pacemaker 1.1.12
##
##=== Amazon AWS i386 AMI's Deprecated ===
##
##Starting with Ubuntu 15.10, i386 AMI's are now deprecated. Users are advised to migrate new workloads to 64-bit HVM instance types. i386 Cloud Images will continue to be published at
##http://cloud-images.ubuntu.com/releases/wily/current for the foreseeable future. 
##
##== Ubuntu Core (Snappy) ==
##
##15.10 is the second release that includes snappy Ubuntu Core, a new Ubuntu rendition that uses a new, ##transactional packaging system: snappy.
##
##‘Snappy’ Ubuntu Core is the smallest and most secure edition of Ubuntu. It is a super-lean, transactionally ##updated version of Ubuntu, perfect for inventors, technologists and the active and growing Ubuntu developer ##community, for cloud container hosts and smart, connected devices. It powers drones, robots, network ##switches, mobile base stations, industrial gateways, and IoT home hubs.
##
##All developers and system builders need to know about the details of this new Ubuntu rendition and how to ##start using snappy Ubuntu Core 15.10 can be found on http://developer.ubuntu.com/snappy.
##
= Known issues =

As is to be expected, with any release, there are some significant known bugs that users may run into with this release of Ubuntu 15.10.  The ones we know about at this point (and some of the workarounds), are documented here so you don't need to spend time reporting these bugs again:

##StartWilyReleaseBugs
== Boot, installation and post-install ==

 * In Virtualbox, the installer currently has a bug where after the installation is complete, the installation medium will eject, but you will be unable to press ENTER to reboot. Powering off and back on should boot you into your installed system. This is being tracked in bug Bug:1447038

 * The amd64 (Intel x86 64bit) images specifically targeted at Apple hardware (amd64+mac) are no longer produced. Most Apple computers are now capable of booting the amd64 image directly using the EFI (not legacy) boot method so long as their firmware is up to date. If for some reason your hardware doesn't boot properly using the amd64 image, make sure you don't have a pending EFI update and if that still doesn't work, then patch the 64-bit ISO using the software in [[https://bugs.launchpad.net/ubuntu-cdimage/+bug/1298894/comments/16|bug #1298894]] (tested working on Macbook 2,1). Alternatively, simply use the i386 (32bit) image instead. 

 * Due to changes in syslinux, it is not currently possible to use usb-creator from 14.04 and earlier releases to write USB images for 15.04 or later; we believe that it is also not possible to use usb-creator from a 15.04 or later system to write USB images for earlier releases.  For now the workaround is to use a matching release of Ubuntu to write the images, but we intend to issue updates soon to work around this incompatibility.  [[Bug:1325801]], Bug:1446646 and Bug:1499746

## * On OEM installations, after the end user configuration in a different language than the default initial ##OEM installation, extra language packs are not installed (Bug:1446539) You can install extra language packs ##by selecting "Language Support" in "System Settings". A dialog will prompt you to install missing language ##packs.

 * During installation on a ''blank disk'' on a UEFI system, if the user creates custom partitions, the installer displays a 'Force UEFI installation?' dialog while there is no pre-installed system (Bug:1447256). This dialog is not displayed if the custom partitioner is not used. This message is harmless since no previous installation exists on the system and you can proceed with the installation.

## * Systems running multipath with a very large number of paths might experience long delays and issues during boot (for example, failure to mount the root filesystem or other filesystems); for details and work-around see bug Bug:1467989.

 * On DELL XPS 13, the EFI partition is wiped if the option "wipe whole disk and install" is selected in the partitioner (Bug:1499323) The EFI partition and the boot can be restored by following the instruction documented in the bug report.

 * Binary drivers installed manually during a live session (for example wifi) are not installed on the completed system (Bug:1508063) The workaround is to either do an installation without pre-installing the drivers in the live session, or after installation, install the drivers from the boot medium.

 * Randomly during installation in Ubiquity only mode (ie not from a live session) unity-system-settings dies unexpectedly (Bug:1508327) resulting in missing or incorrect windows decorations or other visual issues. This has no impact on the installed system and you can proceed with the installation normally

 * golang is now an officially supported language and Ubuntu 15.10 includes golang 1.5, which lacks shared library support. Due to the nature of golang static linking, 3rd party developers desiring bug and security fixes from Ubuntu's updated golang packages will need to rebuild their software with these updates.

== Upgrade ==

 * If several keyboard layouts are configured before upgrade, the wrong layout might be selected after upgrade (Bug:1447157) Re-select the keyboard layout of your choice from the keyboard indicator or system-settings to make it the default. This setting will then persist upon reboot.
## * Ubuntu MATE does not currently support upgrading from 15.04 to 15.10 (Bug:1499078)

##== Power Management ==

##== Desktop ==

##== Migration ==

== Graphics and Display ==

  * AMD's '''fglrx''' driver does not work with the current kernel (Bug:1493888). It is warmly recommended to uninstall the fglrx driver before upgrading to Ubuntu 15.10. The open source "radeon" driver can be used as a temporary replacement until a fix is available.

##== Networking ==

##== Kernel ==


<<BR>>
= Official flavours =

The release notes for the official flavours can be found at the following links:
## * Edubuntu [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/Edubuntu]]
 * Kubuntu [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/Kubuntu]]
 * Lubuntu [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/Lubuntu]]
## * Mythbuntu [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/Mythbuntu]]
 * Ubuntu GNOME [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/UbuntuGNOME]]
 * Ubuntu Kylin [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/UbuntuKylin]]
 * Ubuntu MATE [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/UbuntuMATE]]
 * Ubuntu Studio [[https://wiki.ubuntu.com/WilyWerewolf/ReleaseNotes/UbuntuStudio]]
 * Xubuntu [[https://wiki.ubuntu.com/WilyWerewolf/FinalRelease/Xubuntu]]

<<BR>>
= More information =

=== Reporting bugs ===

Your comments, bug reports, patches and suggestions will help fix bugs and improve the quality of future releases. Please [[http://help.ubuntu.com/community/ReportingBugs|report bugs using the tools provided]].

If you want to help out with bugs, the [[http://wiki.ubuntu.com/BugSquad|Bug Squad]] is always looking for help.

=== Participate in Ubuntu ===

## These images were able to be made available to you thanks to the help of our [[https://wiki.ubuntu.com/SaucySalamander/TechnicalOverview/Beta1/Testers|QA Community]].

If you would like to help shape Ubuntu, take a look at the list of ways you can participate at

 http://www.ubuntu.com/community/get-involved

=== More about Ubuntu ===

You can find out more about Ubuntu on the [[http://www.ubuntu.com|Ubuntu website]] and [[http://wiki.ubuntu.com|Ubuntu wiki]].

To sign up for future Ubuntu development announcements, please subscribe to Ubuntu's development announcement list at:

 http://lists.ubuntu.com/mailman/listinfo/ubuntu-devel-announce
