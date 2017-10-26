# vagrant-spine

> ***Achtung!*** Das Projekt muss lokal auf der Festplatte installiert werden. Es darf nicht im Userprofile (AD) oder auf Netwerkfreigaben installiert werden.
> 20-100 GB Speicherplatz einplanen, damit für das Betriebsystem und für Projekte genug Platz ist.

## Machine Handling

```bash
vagrant up|halt|reload [--provision]
```

Das optionale Argument ```--provision``` sorgt dafür dass das initiale Setupscript ```provision.sh``` erneut ausgeführt wird. Das Script stellt selber sicher,
das nur unterschiede nach installiert werden. Eine Deinstallation von Paketen ist nicht möglich.

## SSH Connection

```bash
vagrant ssh
```

## Webinterface
Nach dem Starten der VM steht ein Webinterface zur verfügung. https://192.168.56.105/

## Mount Project dir

Linux
```bash
sudo mount -t cifs //192.168.56.105/projects -o user=ubuntu -o uid=[local-user] -o gid=[local-group] /mnt/projects
```

Windows
```bash
net use p: \\192.168.56.105\projects
```