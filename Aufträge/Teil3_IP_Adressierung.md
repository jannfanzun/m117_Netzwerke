# Teil 3 IP

## Internet Protocol Adressierung

---

### IP Komponente

- IP-Adresse (Internet Protocol Address): Eine eindeutige numerische Adresse, die Geräten in einem IP-Netzwerk zugewiesen wird, um die Kommunikation innerhalb des Netzwerks zu ermöglichen. Sie kann entweder IPv4 (32-Bit-Adresse) oder IPv6 (128-Bit-Adresse) sein.

- MAC-Adresse (Media Access Control Address): Eine eindeutige Hardwareadresse, die einem Netzwerkadapter zugewiesen wird. Sie besteht aus 6 Byte und wird zur Identifizierung von Geräten in einem lokalen Netzwerk (LAN) verwendet.

- DNS (Domain Name System): Ein System, das die Zuordnung von Domainnamen zu IP-Adressen erleichtert. DNS übersetzt menschenlesbare Domainnamen wie "example.com" in numerische IP-Adressen wie "192.0.2.1".

- Gateway: Ein Netzwerkknotenpunkt, der als Zugangspunkt zwischen zwei unterschiedlichen Netzwerken fungiert. Es ermöglicht die Weiterleitung von Daten zwischen den Netzwerken.

- Subnetzmaske (Subnet Mask): Eine 32-Bit-Nummer, die angibt, welcher Teil einer IP-Adresse zur Netzwerkidentifizierung und welcher Teil zur Host-Identifizierung verwendet wird. Die Subnetzmaske hilft bei der Trennung von IP-Adressen in Subnetze.

- Broadcastadresse: Die höchste Adresse in einem Subnetz, die zur Sendung von Datenpaketen an alle Hosts innerhalb des Subnetzes verwendet wird.

- Netzwerkadresse: Die niedrigste Adresse in einem Subnetz, die zur Identifizierung des Subnetzes selbst verwendet wird und normalerweise für Netzwerkinfrastrukturgeräte wie Router oder Gateways verwendet wird.
- Proxy-Server: Ein Server, der als Vermittler zwischen Clients und anderen Servern fungiert. Der Proxy-Server kann den Datenverkehr überwachen, filtern und optimieren, um die Leistung, Sicherheit und Datenschutz im Netzwerk zu verbessern.

- NAT (Network Address Translation): Eine Technik, die private IP-Adressen in öffentliche IP-Adressen übersetzt und den Datenverkehr zwischen einem privaten Netzwerk und dem Internet ermöglicht. NAT hilft bei der Konservierung von öffentlichen IP-Adressen und bietet eine zusätzliche Sicherheitsschicht für das private Netzwerk.
- DHCP (Dynamic Host Configuration Protocol): Ein Netzwerkprotokoll, das automatisch IP-Adressen und andere Konfigurationsinformationen an Geräte in einem Netzwerk verteilt. Es ermöglicht die dynamische Zuweisung von IP-Adressen an Geräte, die mit dem Netzwerk verbunden sind.
- VLAN (Virtual Local Area Network): Ein logisches Netzwerk, das auf physischen Netzwerkinfrastrukturen aufbaut. VLANs ermöglichen die logische Segmentierung eines Netzwerks, indem sie verschiedene Geräte in virtuelle Netzwerke unterteilen, unabhängig von ihrer physischen Position im Netzwerk.

---

### Netzwerk

- Es gibt im Netzwerk 256 Adresse.
  - Eine Adresse geht an die Netzwerkadresse -> 0
  - Eine Adresse geht an die Broadcastadresse -> 255
  - Es bleiben 254 Adressen
- Wenn die Subnetzmaske 255.255.0.0 ist, dann ist die Netz ID nur 2 Teile gross
  - bsp. IP ist 172.14.23.45
    - Netz ID: 172.14

---

## 11 Aufgabenteil

1. **Bestimmen Sie von der folgenden IP-Adresse die Netz-ID und Host-ID: 192.168.3.37/24**

   - Netz-ID: 192.168.3.0

   - Host-ID: 0.0.0.37




2. **Geben Sie für die folgende IP-Adresse die Netzwerkadresse und Broadcastadresse an: 78.23.49.1231 255.255.255.0**

   - Netzwerkadresse: 78.23.49.0

   - Broadcastadresse: 78.23.49.255




3. **Wie beurteilen Sie diese Adresse: 78.256.125.121255.255.248.0**

   - Ungültige Adresse, da die erste Oktettzahl 256 übersteigt (maximal erlaubt ist 255)




4. **Können Sie Ihrem PC die Adresse 172.30.0.0 vergeben?**

   - Nein, die Adresse 172.30.0.0 ist Teil des privaten Adressbereichs und kann nicht als öffentliche IP-Adresse verwendet werden.




5. **Ihr PC hat folgende Netzwerkeinstellungen: IP: 10.23.65.128/16, Standardgateway: 10.24.0.1 / 16. Wie beurteilen Sie diese Situation?**

   - Sie sind nicht im gleichen Netz. Der Router führt aus dem gleichem Netz.




6. **Welche der beiden Adressen ist eine aus dem privaten Adressbereich: 10.255.255.254 oder 172.25.123.4?**

   - Die Adresse 10.255.255.254 gehört zum privaten Adressbereich.
   - 172.16 - 172.31 sind private Netzwerke




7. **Wie beurteilen Sie diese IP-Adresse: 169.254.0.1/16?**

   - das ist eine APIPA -> Automatische IP Adresse ohne DHCP Server



8. **Wann verwenden Sie diese IP-Adresse: 127.0.0.1?**

   - Die IP-Adresse 127.0.0.1 wird für den Loopback-Test verwendet, um die Netzwerkkarte des lokalen Computers zu testen.




9. **Die beiden folgenden PCs sind über einen Switch verbunden. Die IP-Adressen lauten: 172.16.3.48/24 und 172.16.4.126/24. Können sich die beiden PCs gegenseitig anpingen?**

   - Nein sie sind nicht im gleichen Netz -> die dritte Zahl ist wichtig
   - 3 und 4 sind nicht richtig




10. **Wie beurteilen Sie diese Adresse: 172.22.17.201 mit Subnetzmaske 255.0.0.0?**

    - Die Adresse 172.22.17.201 mit Subnetzmaske 255.0.0.0 gehört zum privaten Adressbereich.
    - Die Subnetzmaske ist unzulässig, da wir eine Private IP haben




11. **Welche Angaben benötigt der Switch und welche der Router, um das eintreffende IP-Paket zu analysieren?**

    - Der Switch benötigt die MAC-Adresse des Zielgeräts, um das Paket an den richtigen Port weiterzuleiten.

    - Der Router benötigt die IP-Adresse des Zielgeräts, um das Paket an das richtige Netzwerk weiterzuleiten.




12. **Ihr Hackerfreund prahlt damit, dass es ihm gelungen sei, die MAC-Adresse seiner Netzwerkkarte zu ändern und damit eine Node-Locked-License zu missbrauchen. Zum Beweis hat er dieselbe MAC-Adresse gewählt wie Ihre. Was ist das Problem dabei und wann könnte der Hack keinen Einfluss haben?**




    - Das Problem besteht darin, dass beide Netzwerkkarten nun die gleiche MAC-Adresse verwenden, was zu Konflikten im Netzwerk führen kann.

    - Der Hack hat keinen Einfluss, wenn die MAC-Adressen auf der Netzwerkschicht (Layer 3) nicht überprüft werden, sondern nur auf der Datenlink-Schicht (Layer 2) verwendet werden.