# Install unsuppported miners in smOS.

I am not affiliated with the Simpleminer team in any way. Just a guy that wants access to the latest miners in smOS.
There is no automatic way to undo what this script does, it can be undone easily with a few linux
commands.

Execute the following command from your smOS CLI where [smOSMiner] is the exact Miner name and version and [URLtoNewMiner.tar.gz] is a url to a tar.gz file of a linux binary.

```
sudo bash -c "$(curl https://raw.githubusercontent.com/davidmoradi/smOS-unsupported-miners/master/install.sh)" - [smOSMiner] [URLtoNewMiner.tar.gz]
```

For example to replace ccminer-tpruvot-v2.1 with t-rex-0.7.4-linux-cuda9.1 the command is:
```
sudo bash -c "$(curl https://raw.githubusercontent.com/davidmoradi/smOS-unsupported-miners/master/install.sh)" - ccminer-tpruvot-v2.1 https://github.com/trexminer/T-Rex/releases/download/0.7.4/t-rex-0.7.4-linux-cuda9.1.tar.gz
```

The smOS miner name must match what is listed on simplemining.net rig groups exactly and include the version number.  Once this script has replaced the miner, you can use smOS gui to make a new rig group for the miner that you replaced but remember it is not the miner that smOS thinks it is, it is the one that you replaced it with.

*It is not recommended to run a script this way unless you trust the source. Please take the time to read the script and do not execute it unless you understand exactly what it is doing.
