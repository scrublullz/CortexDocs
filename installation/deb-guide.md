# Cortex Installation Using a DEB Package

Debian packages are published on Bintray repository. All packages are signed using the key [562CBC1C](https://raw.githubusercontent.com/TheHive-Project/Cortex/master/PGP-PUBLIC-KEY)
(fingerprint: 0CD5 AC59 DE5C 5A8E 0EE1  3849 3D99 BB18 562C BC1C):

```
echo 'deb https://dl.bintray.com/cert-bdf/debian any main' | sudo tee -a /etc/apt/sources.list.d/thehive-project.list
sudo apt-key adv --keyserver hkp://pgp.mit.edu --recv-key 562CBC1C
sudo apt-get update
sudo apt-get install cortex
```

If the command `sudo apt-key adv --keyserver hkp://pgp.mit.edu --recv-key 562CBC1C` fails (because your infrastructure
refuses the acccess to pgp.mit.edu server key), you can run with the equivalent command: `curl https://raw.githubusercontent.com/TheHive-Project/Cortex/master/PGP-PUBLIC-KEY | sudo apt-key add -`

Once the package is installed, please [configure Cortex](../admin/admin-guide.md).
