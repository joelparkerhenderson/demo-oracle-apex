# Oracle Linux DVD ISO + macOS UTM QEMU emulator

For macOS Arm as of 2024-01-01 with UTM QEMU:

1. Get [Oracle Linux DVD ISO](../oracle-linux-dvd-iso/)

2. Get [UTM]()../utm-qemu/)

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


### Reboot

After the VM is created:

1. If the VM reboots, then you might see the Grub prompt with the Oracle Linux DVD ISO options.

2. Eject the ISO by clicking the top right area icon that looks like a CD or DVD, with the tool tip "Drive image options".

3. Reboot. You should see a typical sign in screen.

UTM helpful commands:

* If you want to send special keys to the VM, then turn on mouse capture. Later, use Control+Option to release mouse capture
