# Kis NoSQL attekinto #

## Tutorial ##
A tutorialok futtatasahoz szukseges software-ek
 * ```ipython```
 * ```mongodb```
 * ```redis```

Ezek mind megtalalhatok egy normalis linux distro repository-jaban, de persze
[docker](http://docker.io) segitsegevel is konnyen telepithetoek.

Ezen kivul a ```redis``` alapu demohoz egy ```twitter``` application-t is regisztralnunk kell
a [twitter developer](https://dev.twitter.com) oldalon.

### MongoDB demo ###
A ```notebook``` futtatasa elott eloszor csomagoljuk ki az ```enron.mbox.json.bz2``` fajlt:
```
bunzip2 tutorials/enron.mbox.json.bz2
```

ezek utan inditsunk el egy mongodb instance-t, pl.:
```
mongod --dbpath mdb
```
vagy irjuk at a ```notebookban``` a mongodb elerhetoseget es importaljuk az ```enron.mbox```
fajlt:
```
mongoimport --db enron --collection mbox --file enron.mbox.json
```
