# IT

## Projekte
### Exchange 2016 Projekt
#### Änderungen zu Exchange 2010
- OWA Seite keine Passwortänderung mehr möglich --> So designed von MS
- Office 365 macht ActiveSync, dadurch nur ein Konto direkt mit Exchange verbindbar. Weitere Konten nur über IMAP --> ist bei Mobile Devices jetzt schon so
- UPN muss auf Emailadresse eingestellt sein, da sonst das Autodiscover nicht funktioniert und manche Clients nicht konfiguriert werden können.
- Restore hat nicht alle Funktionen, nur ganze Mailboxdatenbanken können wieder hergestellt werden --> Problem bei Tivoli

#### ToDos

- Nachrichtenfluss --> Sendeconnectors --> ToSmartHost --> Quellservern nur alte Server, wieso?
- Wer schickt an die Exchagne Server? --> MTAs
- Blackberry MDM, alles umgestellt?
-  GSI-Server auf neue Adresse umstellen, wenn sie direkt an Exchange senden
- Mailboxmigration
##### mit Net&Work
- Net&Work: POP für alle standardmäßig deaktivieren
- Net&Work: Beweissicherungsverfahren für alle 3700 Tage aktivieren als Standard für alle Postfächer / Inplacearchivierung einrichten
- Net&Work: ist Active Sync schon bei Client Access auf den neuen Server geändert?
- Net&Work: PublicFolder Mailboxmigration
- Net&Work: Alte Exchangeserver rauskonfigurieren

## Windows

### Server

#### Vertrauensstellung verloren
Reset-ComputerMachinePassword -Server windc07 -Credential campus\winad09

### Exchange 2016

#### IMAP
Test-IMapconnectivity -ClientAccessServer srvex4 -mailboxcredential (Get-Credential campus\skraus)

#### Einen Knoten rauskonfigurieren
1. Datenbank Kopien entfernen
2. aus DAG entfernen (Witness auf SCOM)
3. Check get-clusternode
4. ADSI-Edit Services/MSExchange/GSI --> Einträge überprüfen
5. Exchange Uninstall starten --> z.B. CU Update Installer
6. Empfangsconnectoren kontrollieren

##### Umstellen der Anzahl der Verbindungen:
Warnung:
- Die für InternalConnectionSettings angegebene Portnummer entspricht nicht der für 'UnEncryptedOrTLSBindings/SSLBindings' angegebenen Portnummer. IMAP4-Clients können sich möglicherweise nicht mit dem Dienst verbinden. Mithilfe der Cmdlets 'Get-ImapSettings' und 'Set-ImapSettings' können Sie dieses Problem bestimmen und beheben.
Änderungen an IMAP4-Einstellungen werden erst wirksam, wenn alle Microsoft Exchange-IMAP4-Dienste auf dem Server "SRVEX1" neu gestartet wurden.

#### Updatefehler
Date: Fri Jan 11 2019 10:44:48 GMT+0100
Message: Error: Sys.InvalidOperationException: The following FVA content is not downloaded to client side: LocStringsResource: EditVirtualDirectory, HelpId: EditVDir_InterestingCalendarsEnabled.
Url: https://srvex1.gsi.de/ecp/15.1.1261.39/scripts/wizardproperties.js:1
Line: 86417
Call Stack
ErrorHandling.$Ee@https://srvex1.gsi.de/ecp/15.1.1261.39/scripts/common.js:1:189858
ErrorHandling.showUnhandledException@https://srvex1.gsi.de/ecp/15.1.1261.39/scripts/common.js:1:188929


## Zertifikate
#### Open SSL Pfad
C:\Users\skraus\AppData\Local\OpenSSL-Win32\bin
#### Zertifikatspfad
P:\gsimgr\ManageArea\Zertifikate\20190122_OpenSSLtest
