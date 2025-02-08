# Folding At Home Banano Pi
Earn Banano with Folding at Home

Check also our [YouTube](https://www.youtube.com/@bloxylabs "YouTube") channel for instructions and other related information.

If you had fun with the projects, please consider giving us a Super Thanks on YouTube or buying us a [cup of coffee](https://www.buymeacoffee.com/bloxylabs "cupofcoffee") ☕.


**Command to update the OS:**

```
sudo apt update
```

**Command to upgrade the OS:**

```
sudo apt upgrade -y
```

**Command to download Folding at Home software:**

```
wget https://download.foldingathome.org/releases/public/fah-client/debian-stable-arm64/release/fah-client_8.4.9_arm64.deb
```

**Command to unpack and install software:**

```
sudo dpkg -i --force-depends fah-client_8.4.9_arm64.deb
```

**Command to check the status of the fah-client :**

```
systemctl status --no-pager -l fah-client
```

**Location of config.xml:**

```
/etc/fah-client/config.xml
```

**Command to open nano to edit the config file:**

```
sudo nano config.xml
```

**Code to insert in the config.xml file:**

```
<config>
  <account-token v="YOURTOKEN"/>
  <machine-name v="YOURWORKERNAME"/>

 <!-- See sample config: /usr/share/doc/fahclient/sample-config.xml -->

  <!-- Client Control
       Don't fold anonymously, provide user info. -->
  <fold-anon v='false'/>

  <!-- Folding Slot Configuration -->
  <gpu v='false'/>  <!-- If true, attempt to autoconfigure GPUs -->

  <!-- Slot Control
       Options: light, medium or full
       Watch out for high load -->
  <power v='full'/>

  <!-- User Information
       Send all those points to Banano team -->
  <user v='USERNAME'/>
  <passkey v='YOURPASSKEY'/>
  <team v='TEAMNUMBER'/>

  <!-- Folding Slots -->
  <!-- Use all the CPUs
       Watch out for high load -->
  <slot id='0' type='CPU'/>
  <slot id='1' type='GPU'/>

  <!-- Grant Remote Web Access
       access web UI at 192.168.1.63:7396 -->
  <allow>127.0.0.1 192.168.1.32</allow>
  <web-allow>127.0.0.1 192.168.1.32</web-allow>

</config>
```

**Command to restart the fah-client:**

```
sudo systemctl restart fah-client
```

**Command to stop the fah-client:**

```
sudo systemctl stop fah-client
```

**Command to start the fah-client:**

```
sudo systemctl start fah-client
```
