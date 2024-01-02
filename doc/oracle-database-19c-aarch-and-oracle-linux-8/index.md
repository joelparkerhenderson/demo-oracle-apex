# Oracle Database 19c Aarch64 + Oracle Linux 8


## Install developer release

Become root:

```sh
su
```

Install the Oracle Linux developer release:

```sh
dnf install -y oraclelinux-developer-release-el8
```


## Choose database version

Search for the most-recent Oracle database preinstall package for aarch64:

```sh
dnf search oracle-database-preinstall | grep aarch64
```

As of 2024-01-01, the most-recent result is oracle-database-preinstall-19c.

Install:

```sh
dnf install -y oracle-database-preinstall-19c
```

Oracle Database 19c for Aarch64 is not currently available for download via dnf. 

Launch Firefox and browse:<br>
https://www.oracle.com/database/technologies/oracle-database-software-downloads.html#db_free

The result is currently `LINUX.ARM64_1919000_db_home.zip`.

Download it.

Move it to the conventional place:

```sh
mv LINUX.ARM64_1919000_db_home.zip /tmp/db_home.zip
```


## Make directories

Setup as per installation guide:

```sh
mkdir -p /u01/app/oracle
mkdir -p /u01/app/oraInventory
chown -R oracle:oinstall /u01/app/oracle
chown -R oracle:oinstall /u01/app/oraInventory
chmod -R 775 /u01/app
```


## Configure Oracle user

Set a password for the oracle user, so we can sign in later:

```sh
passwd oracle
```


## Oracle user

Sign out of the `root` user.

Sign in as the `oracle` user.

```sh
mkdir -p /u01/app/oracle/product/19.19/dbhome_1
cd /u01/app/oracle/product/19.0.0/dbhome_1
unzip /tmp/db_home.zip
./runInstaller
```


## Oracle Database 19c installer


### Step 1

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-1.png" alt="Screenshots / Oracle Database 19c installer / Step 1">


### Step 2

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-2.png" alt="Screenshots / Oracle Database 19c installer / Step 2">


### Step 3

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-3.png" alt="Screenshots / Oracle Database 19c installer / Step 3">


### Step 4

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-4.png" alt="Screenshots / Oracle Database 19c installer / Step 4">


### Step 5

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-5.png" alt="Screenshots / Oracle Database 19c installer / Step 5">


### Step 6

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-6.png" alt="Screenshots / Oracle Database 19c installer / Step 6">


### Step 7

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-7.png" alt="Screenshots / Oracle Database 19c installer / Step 7">


### Step 8

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-8.png" alt="Screenshots / Oracle Database 19c installer / Step 8">


### Step 9

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-9.png" alt="Screenshots / Oracle Database 19c installer / Step 9">

https://localhost:5500/em