# Cisco Packet Tracer – LAN

## Popis sítě

Byla vytvořena jednoduchá lokální síť (LAN), která obsahuje:

* 2 switche: **S1, S2**
* 2 počítače: **PC1, PC2**
* 2 servery:

  * **SRV1** – DHCP + DNS
  * **SRV2** – WEB server

### Zapojení:

* PC1 a PC2 jsou připojeny do switch S1
* S1 je propojen se switch S2
* SRV1 a SRV2 jsou připojeny do S2
* konfigurace switchů probíhala pomocí Laptopu přes konzoli

PC1 má staticky nastavenou IP adresu.
PC2 získává IP adresu automaticky pomocí DHCP ze serveru SRV1.

---

## Výpočet X

Příjmení: **LINKA**

| Písmeno | ASCII |
| ------- | ----- |
| L       | 76    |
| I       | 73    |
| N       | 78    |
| K       | 75    |
| A       | 65    |

Součet:

76 + 73 + 78 + 75 + 65 = **367**

Výpočet:

367 mod 256 = **111**

Použitá síť:

**192.168.111.0/24**

Doména:

**linka.cz**

---

## Adresace v síti

| Zařízení          | IP adresa      |
| ----------------- | -------------- |
| S1                | 192.168.111.2  |
| S2                | 192.168.111.3  |
| SRV1 (DHCP + DNS) | 192.168.111.10 |
| SRV2 (WEB)        | 192.168.111.20 |
| PC1               | statická       |
| PC2               | DHCP           |

Default Gateway:

**192.168.111.1**

DNS server:

**192.168.111.10**

---

## Topologie sítě
<img width="886" height="478" alt="Snímek obrazovky 2026-04-16 202923" src="https://github.com/user-attachments/assets/c228cb00-9711-4cd3-a439-536a646d6b60" />

---

## Laptop – konfigurace switchů

<img width="90" height="129" alt="Snímek obrazovky 2026-04-16 194440" src="https://github.com/user-attachments/assets/5cc70106-752c-49a5-ad68-31e43c475908" /><img width="257" height="187" alt="Snímek obrazovky 2026-04-16 194552" src="https://github.com/user-attachments/assets/2e22e320-7138-4573-8dda-a0e5f79602b9" />

<img width="676" height="306" alt="Snímek obrazovky 2026-04-16 194654" src="https://github.com/user-attachments/assets/e3fa98db-9a43-45d8-b5d0-91e51639f60a" />

---

## PC1 – ping (IP + DNS)

<img width="504" height="445" alt="Snímek obrazovky 2026-04-16 194406" src="https://github.com/user-attachments/assets/39775413-101b-435a-a1e4-50e823c5d924" />

---

## Nastavení DHCP (SRV1)

DHCP server přiděluje IP adresy automaticky klientům.

* Start IP: 192.168.111.100
* Subnet mask: 255.255.255.0
* Default gateway: 192.168.111.1
* DNS server: 192.168.111.10

<img width="676" height="306" alt="Snímek obrazovky 2026-04-16 194654" src="https://github.com/user-attachments/assets/3afa74a9-8020-457f-aa48-819b55a84a6b" />

---



## Nastavení SRV1

<img width="869" height="311" alt="Snímek obrazovky 2026-04-16 195613" src="https://github.com/user-attachments/assets/a9f7e903-4641-48b3-82e1-ec1b1ff4c82b" />

---

## Nastavení SRV2 (WEB server)

Na serveru je zapnutá HTTP služba a upraven soubor `index.html`.

<img width="871" height="338" alt="Snímek obrazovky 2026-04-16 195634" src="https://github.com/user-attachments/assets/8ac99f84-9735-49bf-b080-f8cd456f83b7" />

---

## Web – ověření funkčnosti

Po zadání adresy **http://linka.cz** se zobrazí webová stránka.

<img width="834" height="291" alt="Snímek obrazovky 2026-04-16 194742" src="https://github.com/user-attachments/assets/9a7fb031-48dc-49a9-b836-ae375370138c" />


---

## Ověření funkčnosti

* Ping na IP adresu serveru: **funkční**
* Ping na doménu: **funkční**
* DHCP: **funkční**
* DNS: **funkční**
* Web server: **funkční**

---

## Závěr

Síť byla úspěšně nakonfigurována.
Všechny služby (DHCP, DNS, WEB) fungují správně a zařízení spolu komunikují.
