https://github.com/MarcelLison/BSA_Projekt
Info zum Server:

inet 10.76.31.238/20 metric 100 brd 10.76.31.255 scope global dynamic ens18
Password: "bsa"



1.
Aktualisierung mit erstem Befehl die Listen der verfügbaren Pakete und der zweite Befehl installiert alle verfügbaren Paketupdates.

sudo apt-get update && sudo apt-get upgrade

1.1 (Optional) SSH - keygen
ssh-keygen -o -a 100 -t ed25519
    ->ssh-keygen: Befehl zum erstellen von SSH-Key

2. MkDocs installieren:
    https://www.youtube.com/watch?v=WtKa8a4uv3k

    2.1.1 python installiert
    2.1.2 MkDocs installiert
    2.1.3 Docker.io installiert


schriftlich ->      https://docs.techdox.nz/mkdocs/

Tutorial Video ->   https://www.youtube.com/watch?v=K2RDsWgwDTU


inet 10.76.31.238/20 metric 100 brd 10.76.31.255 scope global dynamic ens18

2.2 -> Dockerstarten:
+++
bsa@bsa-u22-server:~/mkdocs$ sudo docker-compose up -d
+++

Fragen:
Wo wird die Glossapp gehostet.
• Welche Dienste laufen auf dem Server?
• Wozu werden die Dienste benötigt?
• Wie greifen die Dienste ineinander?
• Was sollte man wissen wenn man an der Glossapp weiter arbeiten möchte?
• Was gibt es besonders wichtiges für den Admin/Entwickler zu wissen?
• Wer ist für was verantwortlich?
• Welche Frameworks/Technologien kommen zum Einsatz?

--- 

1.
"Hostname" -> 
bsa@bsa-u22-server:~$ hostname
bsa-u22-server
bsa@bsa-u22-server:~$ hostname -I
10.76.31.238 172.17.0.1 172.19.0.1 172.18.0.1
bsa@bsa-u22-server:~$

2.
systemctl list-units --type=service
->

3.Funktion der Dienste -> Name der Dienste und nach Funktion rechachieren. ggf. hilft

4. docker.service und containerd.service:
Der Docker-Dienst steuert die Docker-Engine -> arbeitet mit "containerd" zusammen, um Container zu erstellen, auszuführen und zu verwalten.

5. Um an der Glossapp weiterzuarbeiten, 
solltest du die verwendeten Technologien und Frameworks verstehen 
sowie Zugang zu den entsprechenden Quellcode- und Konfigurationsdateien haben.

6. Ein Admin benötigt Infos wie,
Zugangsdaten, welche Berechtigungen ihm zugewiesen sind, Backup & Wiederherstellungsverfahren sollten ihm bekannt sein.

7. Die Verantwortlichkeit auf einem Server ist im Normalfall so geregelt

Die Verantwortlichkeiten können je nach Organisation variieren. 
Admins sind oft für die Wartung und Sicherheit des Servers verantwortlich,
während Entwickler für die Entwicklung und Wartung der Anwendungen zuständig sind.

8. xxx