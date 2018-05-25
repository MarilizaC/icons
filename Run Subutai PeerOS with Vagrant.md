# Run Subutai PeerOS with Vagrant
The easiest and quickest way to get a Subutai peer running on any platform is to use Vagrant with VirtualBox. Learn how to do a basic setup on Debian Stretch by following the instructions in this guide. 

Before you start, download the required software from their respective websites:
- Vagrant - 2.0.1 or higher
- VirtualBox - 5.0.1 or higher

![Warning](https://github.com/MarilizaC/icons/blob/master/Warning.png) **Warning!** Do not use package managers to avoid installing versions that might be out of date.

With both software installed, you can start creating a Subutai peer VM based on Debian Stretch (version 9.x):

1. Create an initial Vagrantfile (minimal Vagrantfile, in this case):
    ```
    ~$ vagrant init --minimal subutai/stretch
2. Install the subutai and vbguest Vagrant plugins:
    ```
    ~$ vagrant plugin install vagrant-subutai
    ~$ vagrant plugin install vagrant-vbguest
3. Create and start the Subutai peer VM:
    ```
    ~$ vagrant up
    ```
    At one point, you will be prompted to select which bridge interface you want to use. 
    The first option provided by Vagrant is usually the right network interface that is actively being used to connect to the Internet.

##### You’re done!
Congratulations, you now have a peer! Towards the end of the output stream, you should see a message similar to the following:
``` default: SUCCESS: Your peer is up. Welcome to the Horde!
 default: -----------------------------------------------
 default:
 default: Next steps …
 default: Make sure Subutai's E2E Extension/Plugin is installed in your browser
 default: Search for 'Subutai' in your browser's extension/plugin store to find it and install.
 default:
 default: Console URL: https://172.16.1.121:8443
 default: Default u/p: 'admin' / 'secret'
 default:
 default: Vagrant ssh and change the default 'subutai'/'ubuntai' user password!
 default: If you forget the url, just take a look in .vagrant/generated.yml
```
##### What’s Next?
Complete the post-installation procedures to install the companion software: Subutai E2E browser plugin, P2P daemon, and Control Center.	For more information, see the PeerOS and Companion software sections at <span style="color:blue">[Getting Started](https://subutai.io/getting-started.html#E2E).</span>
