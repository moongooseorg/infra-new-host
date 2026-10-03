# infra-new-host

### Image the pi
1. Using the pi imaging software, flash the latest headless 64 bit pi os to an sd card


##### (recommended) Setup easy ssh
If you have never done this before generate a single public/private key.  You only need to run this command once for the rest of eternity
```ssh-keygen```

Then copy the public key to the remote machine
```ssh-copy-id -i <path/to/.pub> pi@192.168.1.1```

### Bootstrap the pi

ssh into the machine and run
```
curl -sSL https://raw.githubusercontent.com/moongooseorg/infra-new-host/scripts/bootstrap.sh | bash
```

##### (note) If your initial system is already setup
Don't forget to register the new host with the github runner