---
layout: post
title: Firmware News (nightly)
author: Stephan Enderlein
category:
- News
- Firmware
---

## Aktueller Stand der Firmware-Entwicklung

Seit Mai 2024 arbeiten wir an einer umfassenden internen Umstellung unserer Firmware. Hintergrund sind tiefgreifende Änderungen in OpenWrt, insbesondere im Bereich Firewall/Netfilter, sowie eine vollständige Überarbeitung unserer Build-Umgebung.
Insgesamt flossen rund **120×8 Stunden ehrenamtliche Entwicklungszeit** in diese Arbeiten.

Die neue Firmware befindet sich nun im **Master-Branch**
- https://gitlab.freifunk-dresden.de/firmware-developer/firmware
und ist aktuell als **Alpha-Version** einzuordnen.

---

## Änderungen im Überblick

### OpenWrt-Anpassungen
- Unterstützung für **OpenWrt 24.10.5** integriert
- Vollständige Überarbeitung der Firewall (**iptables → netfilter**)
- Behebung von Compiler-Fehlern durch neue Toolchain-Versionen
- Rücknahme einzelner OpenWrt-Änderungen, um **Mesh-WLAN-Kompatibilität** sicherzustellen

### Build-Umgebung
- Unterstützung mehrerer OpenWrt-Versionen
- Einführung von **build.json**‑Templates
- Standard-Feed-Revision ergänzt
- Korrektur der **fileinfo.json**‑Validierung
- Optimierung des Feed-Downloads (Fallback/Backup über *dl/*‑Ordner)

### Targets & Router
- Verschiedene Geräte wurden als **EOL** markiert
- Neue Geräte (OpenWrt 24) hinzugefügt

### Web-GUI
- Anpassung der Firewall-Seite an das neue Netfilter-System
- Kleinere Layout-Optimierungen

---

## End-of-Life (EOL) Geräte

Einige Geräte können aufgrund zu geringer Flash-/RAM‑Ressourcen oder fehlender OpenWrt‑Unterstützung nicht mehr mit aktuellen Versionen betrieben werden.
OpenWrt liefert Sicherheitsupdates ausschließlich über neue Releases – daher kann Freifunk Dresden für diese Geräte **keine Updates mehr bereitstellen**.

### EOL‑Targets und betroffene Geräte

#### **[eol.ath79.22.generic] (22.03)**
- Sophos_ap100
- TPLink-tl-wdr3600-v1
- TPLink-tl-wdr4300-v1
- TPLink-tl-wdr7500-v3
- TPLink-tl-wr1043nd-v2
- TPLink-tl-wr1043nd-v3
- TPLink-tl-wr2543-v1

#### **[eol.ath79.22.small] (22.03)**
- Comfast-cf-e110n-v2
- Comfast-cf-e130n-v2
- Comfast-cf-e314n-v2
- Dlink-dir-825-b1
- netgear_wndr3700
- netgear_wnr2200-8m
- TPLink-archer-c6-v2
- TPLink-cpe210-v1/v2/v3
- TPLink-cpe220-v2/v3
- Ubnt_unifi

#### **[eol.sunxi.22.cortexa7] (22.03)**
- Xunlong_orangepi-r1

#### **[eol.ramips.18.rt305x.tiny] (18.06)**
- Dlink-dir-615-d
- Dlink-dir-615-h1

#### **[eol.ar71xx.18.generic] (18.06)**
- TPLink-tl-wr1043nd-v1
- TPLink-tl-wr842n-v1
- Ubnt-bullet-m
- Ubnt-loco-m-xw
- Ubnt-nano-m-xw
- Ubnt-nano-m

#### **[eol.ar71xx.18.tiny] (18.06)**
- TPLink-tl-mr3020-v1
- TPLink-tl-mr3220-v1
- TPLink-tl-wa701nd-v2
- TPLink-tl-wa801nd-v1/v2/v3
- TPLink-tl-wa830re-v