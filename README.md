# IoT Security Analysis – TP-Link Tapo P100

Repozytorium zawiera raport oraz dokumentację **analizy bezpieczeństwa inteligentnego gniazdka IoT TP-Link Tapo P100**, przeprowadzonej w kontrolowanym środowisku laboratoryjnym.

Projekt został zrealizowany w ramach przedmiotu **Bezpieczeństwo Infrastruktury Krytycznej i Systemów Sterowania Przemysłowego (IoT)**.


## Cel projektu

Celem pracy była:
- identyfikacja urządzenia IoT w sieci lokalnej,
- analiza komunikacji sieciowej i mechanizmów szyfrowania,
- ocena potencjalnych podatności i ryzyk,
- sformułowanie rekomendacji zwiększających bezpieczeństwo użytkowania urządzeń IoT.

Badania dotyczyły wyłącznie **własnego urządzenia oraz własnej infrastruktury sieciowej**.


## Badane urządzenie

- Model: **TP-Link Tapo P100**
- Typ: inteligentne gniazdko (smart plug)
- Komunikacja: Wi-Fi 2.4 GHz
- Model działania: chmurowy (aplikacja mobilna ↔ chmura ↔ urządzenie)
- Szyfrowanie komunikacji: **TLS 1.2**


## Środowisko testowe

- Host: Windows
- Wirtualizacja: VMware Workstation
- System testowy: Kali Linux (tryb Bridged)
- Sieć: prywatna sieć Wi-Fi
- Narzędzia:
  - arp-scan
  - nmap
  - tcpdump
  - Wireshark
  - mitmproxy


## Zakres analizy

1. Rekonesans sieciowy urządzenia  
2. Identyfikacja hosta i skanowanie portów  
3. Analiza przechwyconego ruchu sieciowego (PCAP)  
4. Analiza TLS Handshake (SNI, wersja protokołu)  
5. Próba ataku typu Man-in-the-Middle  
6. Przegląd znanych podatności (CVE)  
7. Ocena ryzyka dla użytkownika i sieci lokalnej  


## Wnioski i rekomendacje

- Komunikacja urządzenia jest szyfrowana (TLS), brak transmisji jawnych danych.
- Urządzenie nie udostępnia klasycznych interfejsów administracyjnych w sieci lokalnej.
- Bezpieczeństwo IoT w dużej mierze zależy od konfiguracji sieci domowej oraz konta użytkownika.
- Zalecane środki ochrony:
  - segmentacja sieci IoT,
  - reguły firewall,
  - wyłączenie UPnP,
  - regularne aktualizacje firmware,
  - silne hasła do konta chmurowego.


## Autorzy

- Anna Płaczek  
- Joanna Szewczyk  
- Emilia Zaręba  
- Katarzyna Zieleniewska


## Informacja

Projekt ma charakter **edukacyjny**. Analiza została przeprowadzona bez ingerencji w firmware urządzenia i bez naruszania zabezpieczeń producenta.
