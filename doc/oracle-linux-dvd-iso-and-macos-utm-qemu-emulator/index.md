# Oracle Linux DVD ISO + macOS UTM QEMU emulator

For macOS Arm as of 2024-01-01 with UTM QEMU:

1. Get [Oracle Linux DVD ISO](../oracle-linux-dvd-iso/)

2. Get [UTM](../utm-qemu/)

3. Create a new UTM VM by using the Oracle Linux DVD ISO.

Conventions:

* We prefer to save our iso files in the directory `~/opt/iso/`
  
* We prefer to save our vm files in the directory `~/opt/vm/`

Steps:

1. "Start" dialog:

  * Choose "Virtualize".

2. "Operating System" dialog: 

   * Choose the Custom area "Other".

3. "Other" dialog:

  * Tap "Browse" then find file "OracleLinux-R8-U9-aarch64-dvd.iso".
  
  * Memory: 4096

  * CPU Cores: 1

4. "Storage" dialog:

  * 64 GB
  
5. "Shared Directory" dialog:

  * As is.



### Configure

Choose the language:

* We choose English.

Create root account:

* Check the box to create a root account. 

* Set the password to "changethispassword" or whatever you prefer.

* Click "Done".

Create user account:

* Check the box to create a user account. 

* Set the username to "user" (or whatever you want). 

* Set the password to "changethispassword" or whatever you prefer.

* Click "Done".

Create network settings:

* Turn on Ethernet.

* Set host name to "host-name-example" (or whatever you wish)

* Click "Done".

Eventually you should see a progress bar with the setup process.

After the setup, you should see a message such as "Oracle Linux installation is successful". 

Click the button "Reboot System".


### Reboot

After the VM is created:

1. If the VM reboots, then you might see the Grub prompt with the Oracle Linux DVD ISO options.

2. Eject the ISO by clicking the top right area icon that looks like a CD or DVD, with the tool tip "Drive image options".

3. Type "c" to get a command prompt. Type `reboot` then press return.
   

### License

After the reboot:

1. You should see a license choice. 

2. Accept the license.
   
3. Click "FINISH CONFIGURATION".


### Login

After the configuration:

1. You should see a typical Linux login screen.

2. Log in with username "user" and password "changethispassword" (or whatever you set up earlier).
   
3. Launch a terminal.

Become root:

```sh
su
```

Update the system:

```
dnf --assumeyes update
dnf --assumeyes upgrade
dnf --assumeyes autoremove
```


### Get Oracle Database 

Get Oracle database: [Oracle Database 19c Aarch + Oracle Linux 8](../oracle-database-19c-aarch-and-oracle-linux-8/)


### UTM helpful commands

If you want to send special keys to the VM, then turn on mouse capture. Later, use Control+Option to release mouse capture
