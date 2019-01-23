# IT

## Windows

### Server

#### Vertrauensstellung verloren
Reset-ComputerMachinePassword -Server windc07 -Credential campus\winad09

### Exchange 2016

#### IMAP
Test-IMapconnectivity -ClientAccessServer srvex4 -mailboxcredential (Get-Credential campus\skraus)

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
P:\gsimgr\ManageArea\Zertifikate\20190122_OpenSSLtest
