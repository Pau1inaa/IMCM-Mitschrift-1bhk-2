# IMCM-Mitschrift

Das ist die README.md-Datei. md steht für Markdown. Markdown ist eine im Internet weit verbreitete Auszeichnungssprache (*Markup-Language*). 
Andere bekannte Auszeichnungssprachen sind:

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML, YML)

## Playlist zur Funktionsweise des Internets

![TCP/IP Protokoll und Verwendung von Schichten](/assets/https___miro.medium.com_v2_resize_fit_720_format_webp_1_g1GzSjM5-J3aN2wjVz6qKA.png)

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
- am Ziel wird die Vollständigkeit der Pakete durch das *Transmission Control Protocol* (TCP) überprüft: Wenn Pakete verloren gehen vordert TCP die erneute Übertragung an. TCP und IP bilden gemeinsam die Basis für die Funktionsweise des Internets - man spricht auch vom TCP/IP-Modell.

### Teil 5 - The Internet: HTTP and HTML

- das *Hypertext Transfer Protocol* (HTTP) ist das Protocol das für die übertragung von Websiten verwendet wird
- der Ablauf ist immer der sekbe:
    1. der Web-Client (Browser) schickt eine HTTP-Anfrage (*Request*) an den Web-Server
    2. der Web-Server antwortet übernimmt die Anfrage bearbeitet sie und schickt eine Antwort (*Response*) zurück an den Client. Dabei versieht er die Antwort mit einem [HTTP-Statuscode](https://de.wikipedia.org/wiki/HTTP-Statuscode). Diese sind in verschiedenen Klassen eingeteilt.

    
    > #### HTTP-Statuscode-Klassen
    >
    > **1xx** - die Anfrage dauert noch an
    >
    > **2xx** - die Anfrage war erfolgreich
    >
    > **3xx** - Weiter- oder Umleitung
    >
    > **4xx** - Clientfehler (z.B. 404 - Not Found)
    >
    > **5xx** - Serverfehler

- Daten (Websiten, Bilder, Videos, usw.) werden mittels GET-Anfragen angefordert
- User-Imput (Texteingaben, Dateiuploads, ...) werden mittels POST-Anfragen verschlüsselt übermittelt
- GET und Host sind sogenannte **HTTP-Methoden**. Es gibt noch weitere Methoden die wir erst später lernen.
- HTTP-Anfragen und Antworten können auch **Cookies** enthalten. Das sind kleine Textdateier die aus Schlüssel-Wert-Paaren (*key-value-pairs*) bestehen. Ist ein Cookie einmal besetzt wird es mit jeder Anfrage mitgesendet. So kann der Webserver einzelne User wiedererkennen bzw. identifizieren.

### Teil 8 - The Internet: How Search Works

- Suchmaschinen-Bots (*Crawler*) durchstreifen ständig WWW und katalogisieren Websites. Der so entstehende Katatlog wird auch **Index** genannt
- wenn wir einen Suchbegriff bei Google (oder einer anderen *Serach Engine*) eingeben, wird NICHT das WWW durchsucht, sondern lediglich der zuvor erstellte Index
- Suchergebnisse werden auf Basis eines (geheimen) Algorithmus geranked - Ergebnisse, die weiter oben stehen, werden öfter angeklickt
- Einfluss auf das Ranking haben u.a.:
    - im Text vorkommende Suchbegriffe (*Keywords*)
    - Links, die auf meine Seite zeigen (*Backlinks*) 
- die Suchergebnisse werden an die Benutzer*innen angepasst! D.h., nicht jede/r sieht die gleichen Informationen, selbst wenn sie idente Suchanfragen durchführen!
- [Startpage](https://www.startpage.com/) ist eine datensparsame Suchmaschine, die ihren Benutzer*innen die Verwendung von Google ohne Tracking oder Personalisierung erlaubt

---

### Ergänzung: Überblick über das TCP/IP-Modell

Im TCP/IP-Modell übernimmt jede Schicht eine eigene Aufgabe (merke: *"divide and conquer"*), hat einen eigenen Namen für die versendeten Dateneinheiten und einen eigenen Adressierungsmechanismus:

| Schicht | Protokoll | Dateneinheit | Adressenmechanismus |
|---      | ---       | ---          | ---                 |
| Internet| IP        | Paket        | IP-Adressen         |
|Transport| TCP       | Segment      | Ports               |
| Link    | Ethernet  | Frame        | MAC-Adressen        |

Die Daten der Anwendungsschiicht werden auf der Transportschicht in ein Segment verpackt.  Dieses wird in der Internetschicht in ein Paket verpackt; und dieses schlussendlich in der Link-Schicht in ein Frame.


![Datenkapselung im TCP/IP-Modell](/assets/segment-packet-frame.jpg)

---

## Webtechnologien: HTML, CSS und JS

![HTML-CSS-JS](/assets/html-css-js.png)

### HTML - *Hypertext Markup Language*

HTML gibt den Inhalten einer Website die Struktur vor. Die `index.html` ist üblicherweise der zentrale Einstiegspunkt für jede Website - alle weiteren Inhalte (Bilder, Videos, CSS-Stylesheets, JS-Skripte, usw.) werden über diese verknüpft.

Die zentralen Bausteine von HTML sind sogenannte **Tags**. Tags können mithilfe von Attributen erweitert werden. Attribute sind Schlüssel-Wert-Paare (*key-value pairs*). Der HTML Quellcode einer Website wird vom Browser und von Suchmaschinen-Bots (*Crawler*) gelesen und interpretiert.

![HTML-Syntax](/assets/https___codetheweb.blog_assets_img_posts_html-syntax_tag-structure-2.png_%20class=_transparent)

Ein HTML-Dokument ist hierarchisch aufgebaut. Wir sprechen in diesem Zusamenhang auch vom **DOM-Tree** (*Document Object Model*). Jedes HTML-Dokument ist aufgebaut wie ein Baum. Die Wurzel des Baumes ist der `<html>`-Tag. Auf der nächsten Ebene befinden sich die beiden Tags `<head>` und `<body>`. Im `<head>` finden sich in erster Linie Metadaten, die Informationen über dke Webpage enthalten, z.B. der Titel der Seite , die Sprache, die Zeichenkordierung usw. Im `<body>` finden sich die eigentlichen Inhalte der Webpage, z.B. Texte, Bilder, Videos, Links, usw.