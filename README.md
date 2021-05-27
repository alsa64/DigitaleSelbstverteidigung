# DigitaleSelbstverteidigung

Anhaltspunkte zur digitalen Selbst-Verteidigung.

## Windows 10

### Essentielle Links:

#### [Netzwerkverbindungen von Windows Komponenten Reduzieren](https://docs.microsoft.com/en-us/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services=)

Für die meisten dieser Optionen ist leider eine Microsoft Windows 10 pro Version oder höher erforderlich.

Generell ist anzumerken, dass die meisten Privatsphäre Tools, die versprechen mit einem Klick alle Probleme zu lösen, Placebo Effekte auslösen und oft sogar für Probleme sorgen. Generell würde ich daher immer empfehlen, diese Veränderungen manuell vorzunehmen. Denn nur dann ist es möglich nachzuvollziehen, was genau man denn eigentlich gerade macht.

#### [Windows 10 Release Health Monitor](https://docs.microsoft.com/en-us/windows/release-health/)

Immer wieder treten bei Windows 10 Updates große Probleme auf. Beispielsweise gelöschte Dokumente Ordner, Bootloops für Leute mit gewissen SSDs, oder gar ein unbenutzbarer Computer, weil man beispielsweise ein anderes Antivirenprogramm als Microsoft Defender benutzt hat.

Die meisten dieser Probleme sind schon Wochen vor der Herausgabe der jeweils neuen Windows Version bekannt. Auf dieser Webseite kann man sie nachlesen und nachschauen ob man von einem dieser Probleme betroffen ist, oder nicht.

#### Zu Antivierenprogramme

Generell würde ich von der Installation alternativer Antivirenprogramme abraten.

Viele von ihnen werben mit einer Angstmacherei. Der Schutz von Microsoft Windows Defender recht völlig aus.

Leider hört man auch immer wieder Empfehlungen, Antivirenprogramme komplett zu deaktivieren. Generell ist das allerdings keine gute Idee. Es ist höchstens dann dazu zu raten, wenn die Maschine nie mit dem Internet verbunden wird Oder hinter einer starken Firewall mit einer Whitelist steht.

## Passwortsicherheit

In der Vergangenheit wurde oft zu Passwörtern aus komplett zufällig generierten Buchstaben, Zahlen, und Sonderzeichen geraten, diese haben aber oft das Problem dass sie schwer zu merken sind, und dass sie in der Regel eher kurz sind, da wir uns lange zufällige Passwörter nicht merken können. Oft verwenden wir auch das selbe Passwort oder das selbe Passwort in Variationen.

Mein Lösungsvorschlag ist stattdessen einen Passwort Manager zu benutzen. Dabei kann ich besonders die Passwort Manager Bitwarden und KeepassXC/Keepassium empfehlen.

Ein Passwort Manager speichert alle Passwörter verschlüsselt hinter einem anderen Passwort ab. Das bedeutet, dass man sich nur ein Passwort merken muss wie ist das Passwort kann dann auch entsprechend sicher sein. Das ist natürlich auf dem Bad ein neues Problem, wenn jemand Zugriff auf euren Passwort Manager und euer Master Passwort bekommen bedeutet das dass er auf alle anderen Accounts ebenfalls Zugriff bekommt. Daher ist es essenziell, mindestens ein sicheres Passwort zu benutzen aber besser noch einen Zweit Faktor hinzu zu fügen.

Für das Master Passwort selbst, empfehle ich einfach 3-5 deutsche Wörter zu nehmen, und diese mit einem Sonderzeichen jeweils zu verbinden. Als Menschen fällt uns das merken solche Passwörter um einiges leichter.

![password_strength.png](https://imgs.xkcd.com/comics/password_strength.png )

### [Bitwarden](https://bitwarden.com/)

[Bitwarden](https://bitwarden.com/) ist leichter zu bedienen und hat die bessere Browser Integration. Es ist Open Source und lässt sich selbst hosten. Wenn man das nicht möchte, kann man auch völlig kostenlos unbegrenzt viele Passwörter auf dem Haupt mit warnen Server speichern. Dabei werden die Passwörter auf allen Geräte synchronisiert. Es erlaubt das automatische Ausfüllen von Passwörtern, Kontaktdaten, und Kreditkarten. Weiterhin können sichere verschlüsselte Notizen angelegt werden.

Für die meisten Nutzer würde ich Bittwarden warten empfehlen.

### Keepass

Auf KeePass basierende Passwort Manager, wie [KeePass XC](https://keepassxc.org/) (Windows, Linux, macOS), [KeePass DX](https://www.keepassdx.com/) (Android) und [KeePassium](https://keepassium.com/) (IOS), und andere Derivate von KeePass, setzen auf eine etwas andere Herangehensweise. Sie speichern alle Passwörter in einer verschlüsselten Datenbank in einer Datei ab. Diese Datei kann man dann auf Wunsch auch in eine Cloud packen um sie zu synchronisieren. Der Vorteil dieser Herangehensweise ist dass man selbst unter Kontrolle hat wo die Daten gespeichert werden. Das hat man bei [Bitwarden](https://bitwarden.com/) beispielsweise nur wenn man den Server selbst hostet. Die Integration in die Browser ist nicht so gut, aber KeePass ist immer noch sehr interessant für Leute die die absolute Kontrolle behalten wollen.

### Andere Passwortmanager

Ich rate von anderen Passwort Manager wie LastPass, NordPass, 1Password, Enpass, und so weiter ab. Da der Passwort Manager alle Passwörter verwaltet, ist das meiner Meinung nach essenziell, dass mindestens der Client des Passwort Managers selbst Open Source sein muss.

## Multi-Faktor Authentifizierung (acuh 2fa oder OTP)

Die Idee der Multifaktor Authentifizierung ist mehrere Anmeldeoptionen zu kombinieren.
Generell unterscheiden wir zwischen drei verschiedenen Arten von Faktoren.

- Etwas was man weiß. Wie beispielsweise ein Passwort, oder eine PIN, oder die Antwort auf eine Frage.

- Etwas was man hat. Wie beispielsweise eine Bankkarte, oder ein Gerät, oder ein Hardwareschlüssel

- Eine Biometrische Eigenschaft. Beispielsweise ein Fingerabdruck, die eigenen Augen, die Gesichtsform, ...

Falls man einen Passwort Manager benutzt, rate ich stark dazu einen zweiten Faktor einzurichten. Ich selbst benutze dafür beispielsweise einen Hardwareschlüssel (YubiKey), Aber auch eine klassische zwei OTP App auf dem Handy kann das tun.

### One Time Password (OTP)

Das ist die wahrscheinlich häufigster Variante eines Zweit Faktors für die meisten Webseiten und Programme. Es handelt sich um einen in der Regel sechsstelligen Code, der alle 30 Sekunden ein anderer ist. Er wird aus einem langem Schlüssel errechnet.

Die meisten Passwort Manager unterstützen auch das abspeichern von OTP Schlüsseln, das sollte man allerdings nur dann tun, wenn der Passwort Manager selbst mit einem zweiten Faktor geschützt ist. Wenn der Passwort Manager auch die zwei Faktor Authentifizierung von Webseiten Managed, kann er natürlich dieses Feld auch automatisch ausfüllen.

Ansonsten sollte man einfach eine App auf dem Smartphone, Oder einen zweiten Passwort Manager nur für den Zeitfaktor benutzen.

## VPNs

[![Videoempfehlung](http://img.youtube.com/vi/WVDQEoe6ZWY/0.jpg)](https://www.youtube.com/watch?v=WVDQEoe6ZWY)

Zusammengefasst:

VPNs finanzieren Werbeclips am Anfang oder Ende von vielen Lehrvideos. Dabei werben sie mit Versprechen, die sie nicht oder nicht überprüfbar einhalten können.

- "VPNsschützen vor Daten Diebstahl."

Viele VPNs erwecken in ihrer Werbung den Eindruck, dass jeder, der im selben Netzwerk ist, die Login Daten der Nutzer des Netzwerkes abfangen kann. Das ist in der Tat möglich, allerdings nur für Webseiten die mit HTTP beginnen nicht für Webseiten, die mithttpsbeginnen. Diese sind verschlüsselt und andere Netzwerk Teilnehmer sowie der Internetanbieter können höchstens die Domain sehen (Beispielsweise: **https://duckduckgo.com**/?t=ffab&q=das+sehe+nur+ich&ia=web, nur der Fettgedruckte Teil kann von einem drittem gesehen werden). Die gesamte Kommunikation mit der Webseite verläuft verschlüsselt. 

- "VPNs waren deine Privatsphäre"

Das ist halb korrekt, durch das benutzen einer VPN wird effektiv der Internet Anbieter ausgetauscht. Der eigene Internet Anbieter und Netzwerkbetreiber, kann nicht mehr sehen welche Domäne wir aufrufen, dafür kann es allerdings der VPN Betreiber.

Viele VPN Anbieter werben weiterhin damit, dass sie nicht IP loggen, das lässt sich allerdings nicht überprüfen und man sollte solche Versprechen mit gesunder Skepsis wahrnehmen.

Manche gehen sogar soweit, zu behaupten dass gar keine Spuren hinterlassen werden, das ist im Internet aber unmöglich.

---

Das alles heißt nicht das VPNs keine validen Zwecke haben können.

Beispielsweise um Zensuren zu umgehen. Gerade an manchen restriktiven Schulen, Universitäten, und anderen Institutionen, wird das Internet gerne gefiltert. Durch eine VPN, kann man ein unzensiert das Internet benutzen. Oder zumindest so unzensiert wie ist der Standort des VPN Servers erlaubt. Ebenfalls verhindert ist, dass die jeweilige Institutionen oder Personen, die das Netzwerk überwachen kann, Rückschlüsse auf sensible Daten wie Sexualität, Religiosität, und andere ziehen kann, die gegen die eigenen Werte entgegen gehen.

Ebenfalls können VPNs praktisch sein, um von und auf Geräte im Heimnetzwerk außerhalb des Heimnetzwerkes zugreifen zu können, dazu muss man sie aber selber hosten.

## Linux

Wer ganz auf Windows verzichten kann, sollte Linux in Betracht ziehen. Dabei handelt es sich um ein alternatives Betriebssystem, dass komplett Quelle offen ist. Selbst viele Windows Programme lassen sich auf Linux einfach ausführen, für die meisten von euch bedeutet das, dass er einfach Simon geniert, das Spiel eurer Wahl ausfällt, und das spielen drückt.

Steam Play / Proton Ist in der Lage, die meisten Windows Spiele einfach auf Linux zu übersetzen. Manche Spiele laufen dadurch sogar schneller, andere etwas langsamer. Auf Proton DB kann man nachlesen, welche der Spiele laufen und welche nicht. Vielleicht ist das für den ein oder anderen von euch eine Option.

Dabei kommt Linux in der Form von Distribution also Kombinationen an Programmpaketen. Generell ist die Auswahl davon relativ egal, ihr könnt auch so ziemlich jeder von ihnen machen was ihr wollt. Ich selbst benutze Arch Linux, diese ist allerdings für neue Nutzer etwas schwieriger zu erlernen und installieren.

Meine generelle Empfehlung für Interessierte wäre [Manjaro](https://manjaro.org/), [EndeavourOS](https://endeavouros.com/), [Pop!_OS](https://pop.system76.com/). Für die absoluten Kontrollfreaks unter euch, die die absolute Kontrolle über ihr System haben wollen, sind [Arch Linux](https://archlinux.org/) und [Gentoo](https://www.gentoo.org/) wahrscheinlich am interessantesten, Beide lassen den Nutzer ihr System von Grund auf selbst gestalten, das macht sie allerdings auch deutlich schwieriger zu erlernen, und für Anfänger zu installieren. Die Dokumentation ist umfassend, wer sich also trauen will, nur zu, macht den Sprung ins kalte Wasser.

## Netzwerkprojekte

### PiHole / AdGuard Home

Um zu verstehen was PiHole, und Adguard Home machen, muss man zuerst wissen was ein DNS Server ist. Ein DNS Server liefert auf eine Anfrage zu einer Webseite dessen eigentliche Adresse die so genannte IP Adresse zurück. Über diese IP Adresse, kann dann die eigentliche Webseite oder Inhalte aus dem Internet geladen werden.

Ein PiHole, oder AdGuard Home, ist ein selbst gehosteter DNS Server, der auf Wunsch manche Anfragen nicht beantwortet.

Fragt der Computer beispielsweise nach der IP Adresse von google.de, erhält er die Adresse von google.de, fragt er allerdings beispielsweise nach werbung.de oder Windows10telemetrie.com, bekommt er nichts zurück.

Anders als die meisten werbe Blocker, die man beispielsweise in einem Browser installiert, funktioniert das Netzwerkwald das bedeutet es betrifft alle Geräte, die im eigenen WLAN oder per LAN Kabel verbunden sind.

Der Vorteil dieses Ansatzes ist, dass er auch für Werbung außerhalb von Web Browsern schützt, ganz geschweige denn von den vielen Geräten, auf denen eine Installation eines Werbeblockers gar nicht möglich ist, wie ein Smart TV oder eine Spiele Konsole.

Solch ein Gerät lässt sich sehr günstig herstellen. Eine typische Konfiguration wird mit einem Raspberry Pi gemacht.

Ich denke, das ist ein Projekt dass viel mehr Sicherheit und praktische Vorteile geben würde dass sich günstig und relativ einfach umsetzen lässt. Dabei erlernt man ebenfalls einige Linux Skills.

### Firewall

Ein anderes Projekt wäre die Einrichtung einer Firewall im eigenen Netzwerk. Persönlich empfehle ich [OPNsense](https://opnsense.org/), Dieses erfordert aber Einen auf Intel/AMD x68_64 basierenden PC/Server. Das bedeutet, dass die Einrichtung eines solchen etwas teurer in der Anschaffung ist. Man kann beispielsweise einen Intel NUC verwenden. Generell muss der PC nicht viel Leistung haben, etwas günstiges reicht. Die Einrichtung ist leichter wenn der PC zwei Ethernet Anschlüsse hat (man kann auch einen USB zu Ethernet Adapter benutzen), kann aber auch mit einer Managed Switch (~25-30€) über VLAN tagging umgesetzt werden wenn nur ein Anschluss vorhanden ist.

Alternativ, kann man auch eine beliebige andere Linux oder PSD basierende Firewall benutzen, und einen günstigen Raspberry Pi oder anderes Arm basierendesgerät dafür verwenden. Wer eine grafische Benutzeroberfläche im Internet haben will, ist beispielsweise auch mit [OpenWRT](https://openwrt.org/) gut aufgehoben.
