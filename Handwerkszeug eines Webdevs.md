Wenn wir eine Webseite schreiben wollen, müssen wir uns erstmal Gedanken über die grundlegende Struktur machen. Welche Elemente sollen auftauchen, welche nicht? Welche Unterseiten soll es geben? Wie navigiert der Nutzer auf der Webseite? Wie sollen Elemente aussehen und wie nicht? Dies alles fällt unter das Stichwort [[Web-Design]]. 

Sobald dies entschieden ist kann man sich dem Development widmen. Dafür müssen erstmal alle Elemente definiert werden, die auf der Website auftauchen sollen. Es muss also die Struktur der Website festgelegt werden. Dies wird in [[HTML]] umgesetzt.

Danach folgt die Anpassung des Aussehens der Website. Die Ergebnisse des Web-Design Prozesses werden dafür in [[CSS]] umgesetzt. 

Falls es nötig wird Informationen auf der Website zu aktualisieren, muss man eine Website dynamisch gestalten. Dafür nutzt man i.d.R. [[JavaScript]]. Andere Programmiersprachen ermöglichen dies zwar auch, aber JavaScript wurde speziell dafür entwickelt.

# Frontend und Backend

Es wird beim Webdevelopment in zwei Bereiche unterschieden: Frontend und Backend. Das Frontend bezeichnet die Oberfläche, mit der der Nutzer interagiert. Das Backend stellt Daten bereit, die dann im Frontend dargestellt werden oder z.B. für das Login genutzt werden können. Das Backend besteht daher i.d.R. mindestens aus einer Datenbank, kann aber auch sehr viel mehr tun. HTML und CSS sind Frontend-Technologien, während JS für beides eingesetzt werden kann.
# Web-Frameworks

Diese grundlegenden Technologien wurden im Laufe der Zeit durch verschiedene Frameworks erweitert. Diese ermöglichen erweiterte Funktionalitäten oder vereinfachen den Entwicklungsprozess. Es wird in Frontend- (z.B. React)und Backend-Frameworks (z.B. Express.js) unterschieden. 


# Dev-Ops

Die Schnittstelle zwischen der Entwicklung einer App und dem Bereitstellen und Hosting für den Nutzer nennt sich Dev-Ops (von Development und Operations). In der Regel beschäftigt man sich bei Dev-Ops mit den unten genannten Problemen.
## Hosting-Lösungen

To Cloud or not to Cloud, das ist hier die Frage. Meist entscheidet man sich für eine Cloud-Lösung allerdings können Regularien, wie Datenschutz-Recht, eine hybride Architektur diktieren. Falls man sich für die Cloud entscheidet, muss man außerdem den passenden Provider auswählen. Das macht man in der Regel von den Kosten und den Features, die der Provider bereitstellt, abgängig.

## Provisioning und Deployment

Provisioning bezeichnet das Bereitstellen von IT-Infrastruktur. Deployment bezeichnet das Bereitstellen von Software für den Nutzer.

## IaC

Provisioning kann vor allem durch Infrastructure as Code (IaC) vereinfacht werden. Dabei wird mit Hilfe von Programm-Code und/oder Config-Dateien die Bereitstellung von Infrastruktur automatisiert. Teilweise kann sogar die Erstellung eines Deployment-Environments automatisiert werden. Bespiel: Ansible

## CI/CD

Continous Integration / Continous Delivery bezeichnet die Automatisierung des Entwicklungs- und Bereitstellungsprozesses von Software. Dies erfolgt meist mit Hilfe einer Pipeline. Beispiel: GitHub-Actions