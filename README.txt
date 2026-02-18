Analisi di Vulnerabilità Slowloris con Strumenti di Sicurezza
Descrizione del Progetto
Questo progetto dimostra come identificare, analizzare e sfruttare vulnerabilità in un ambiente virtuale controllato. Utilizza una macchina con Ubuntu Server (server vulnerabile) e una macchina con Kali Linux (attaccante)
Requisiti
•	VirtualBox: per eseguire l'applicazione vulnerabile in un ambiente isolato
•	Ubuntu Server e Kali Linux
Le Assunzioni Fatte per l'Attaccante
Accesso alla Rete
•	L'attaccante è connesso alla stessa rete locale del server vulnerabile. 
Da Dove Parte l'Attacco
•	L'attacco viene eseguito da una macchina virtuale con Kali Linux (kali-linux-2025.4-virtualbox-amd64) ospitata sullo stesso hypervisor (VirtualBox).
Compiti e Configurazioni del Server Sotto Attacco
•	Sistema Operativo: macchina virtuale con Ubuntu Server (ubuntu-24.04.1-live-server-amd64).
•	Servizi Attivi: 
o	Apache2: server web per servire la pagina vulnerabile.
o	MySQL: database in cui sono salvati i dati
•	Applicazione Vulnerabile: 
o	Una pagina HTML dalla quale poter visualizzare dei dati 
•	Rete e Accessibilità: 
o	Configurazione della rete in Virtual BOX.
	NAT
	Host-Only
o	Inidirizzi IP assegnati tramite DHCP
Installazione
Server Target (Ubuntu)
(vedi configurazione completa nel powerpoint)

Macchina Attaccante (Kali Linux)
•	Browser Web (Firefox):
È preinstallato in Kali Linux.
•	Wireshark:
È preinstallato in Kali Linux.
Sniffare il Traffico di Rete con Wireshark
1.	Avvia Wireshark e cattura i pacchetti HTTP.
2.	Osservare il volume di richieste inoltrate ed il tempo di attesa
Risultati
•	Web Application praticamente resa inutilizzabile per usufruire dei dati
•	Traffico HTTP Analizzato con Wireshark:
Screenshot del traffico HTTP, evidenziando il comportamento.
Struttura del Repository
•	SlowLoris.pptx: presentazione PowerPoint con attacco documentato
•	elezioni_2025: dump del database MySQL di esempio.
Disclaimer
Questo progetto è inteso solo per scopi educativi e di ricerca. Non è permesso l'uso di queste tecniche su sistemi non autorizzati. L'autore non si assume alcuna responsabilità per eventuali danni derivanti da un uso improprio.

