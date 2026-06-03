# IMCM-Mitschrift

Das ist die README.md-Datei. md steht für Markdown. Markdown ist eine im Internet weit verbreitete Auszeichnungssprache (*Markup-Language*). 
Andere bekannte Auszeichnungssprachen sind:

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML, YML)

## Playlist zur Funktionsweise des Internets

### Teil 1 - What is the Internet?

- wurde in den 1970 Jahren erfunden
- Motivation: Schaffung eines dezentralen Netzwerks, das auch nach einem Atomschlag noch funktioniert (Kontext des Kalten Krieges)
- Funktionsweise Paketvermittlung (*Paket Switching*) - jedes Datenpaket sucht sich eine eigene Route durch das Netzwerk
- Internet: das Netz der Netze - besteht aus vielen kleinen Netzen unterschiedlicher Internetanbieter (*Internet Service Provider - ISP*, z.B.: A1, Magenta, Salzburg AG, ...)

### Teil 2 - The Internet: Wires, Cables and Wifi

Informationen werden im Internet als Bits übertragen. Bits haben zwei Werte: 0 oder 1. 8 Bits ergeben 1 Byte. Mit einem Byte kann man 256 verschiedene Werte speichern (2^8 = 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2).

Bits können über verschiedene Übertragungsmedien zwischen Computern versendet werden. Die Anzahl der Übertragenen Bits pro Sekunde wird als Bandbreite bezeichnet - z.B.: 300MBit/s -> 300 Millionen Bit können pro Sekunde über diese Leitung laufen. Übertragungsmedien können sein:

1. Kupfer / Elektrizität
    - billig
    einfach in der Verarbeitung
    - weit verbreitet
    - hohe Verluste über lange Distanzen (hunderte Meter)

2. Glasfaser / Licht
    - schnelle Übertragung 
    - verlusttfrei
    - geeignet für Ozeankabel
    - teuer und schwierig in der Verarbeitung

3. Funk / Radiowellen
    - hoher Komfort, Internet überall
    - hohe Verluste über Distanzen

### Teil 3 - The Internet: IP-Adresses & DNS

- Protokolle sind die Regeln der Kommunikation
- eines der wichtigsten Protokolle im Internet ist das Internet Protocol (IP)
- jedes Gerät im Internet hat zumindest eine (eindeutige) IP-Adresse, viele Geräte haben aber eine externe IP (ähnlich wie die Raumnummer)
- das Domain Name System (DNS) übersetzt menschenlesbare Domainnamen (z.B.: www.google.com) in IP-Adressen
- DNS-Server führen Tabellen mit Domainnamen und den entsprechenden IP-Adressen

### Teil 4 - The Internet: Packets, Routing and Reliability

- Daten die über das Internet versendet werden, werden in Pakete aufgeteilt
- Pakete sind in der Regel rund 1500 Byte groß (=1.5 KB). Das heißt ein 10MB großes Foto würde in etwa 6667 Pakete aufgeteilt werden (10MB = 10.000KB = 10.000.000 Byte / 1500 Byte = 6667 Pakete)
- Pakete können unterschiedliche Routen durch das INternet nehmen. Die Routenplanung erfolgt durch spezielle Computer - sogenannte Router. Router entscheiden, welchen Weg ein Paket durch das Internet nimmt. Die Entscheidung basiert auf verschiedenen Faktoren, wie z.B. der aktuelle Auslastung der Verbindungen und der Entfernung zum Ziel.
- jedes Paket enthält die IP-Adressen der Quelle und des Ziels sowie die Reihenfolge der Pakete (damit sie am Ziel wieder korrekt zusammengesetzt werden können)