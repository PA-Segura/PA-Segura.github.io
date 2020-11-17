# How to make 10 000 points measurements with a [miniVNA pro](http://miniradiosolutions.com/minivna-pro/){:target="_blank"} and make time domain analysis

Here I describe how you can use your low-cost VNA miniVNA pro to make sweeps of 10 000 points. Then you can use these bunch of points to make time-domain analysis or a gating filtering using the [scikit-rf](http://scikit-rf.org/){:target="_blank"} python library. 

Time-domain analysis can be of interest in the analysis of the time reflections finding 


I haven't fond if it is possible to carry out these type of measurements with the graphical interface of the miniVNA, but using the headless version is possible by just asking for it (in the case of an s21 measurement): 

```
java -Dfstart=10000000  -Dfstop=50000000  -Dfsteps=10000  -DdriverId=2  -DdriverPort=ttyUSB0 -Dcalfile=/home/pi/vnaJ.3.3/calibration/TRAN_miniVNA-pro10000.cal -Dscanmode=TRAN  -Dexports=snp  -DexportDirectory='/home/pi/vna/data' -DexportFilename='VNA_{0,date,yyMMdd}_{0,time,HHmmss }' -Duser.home=/home/pi/ -Duser.language=en -Duser.region=US -DnumberOfScans=3 -jar /home/pi/vna/vnaJ-hl.3.3.3.jar
```

_Previously I have carried out a calibration (in the GUI) that corresponds with these 10 000 points_ (it has to be done with the same version of your head less executable in this case 3.3.3)

After running the comand your miniVNA will take some time doing the measurements and will deliver some s2p files, then you can analyze these files with scikit-rf to carry out gating or other operations over your s2p file.

--------------
2020-11-01
