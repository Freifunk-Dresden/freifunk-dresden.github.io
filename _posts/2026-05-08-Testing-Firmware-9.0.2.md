---
layout: post
title: Testing Firmware 9.0.2
author: Stephan Enderlein
category:
- News
- Firmware
---
Testing Firmware [9.0.2](https://download.freifunk-dresden.de/firmware/testing-9.0.2/).

Diese Testing Firmware beinhaltet große aber auch kleinere Änderungen und Verbesserungen. \
Die Firmware basiert auf Openwrt, welche seit einigen Jahren den Support für Router mit zu kleiner
Leistung und Speicher eingestellt haben. \
Für viele alte Router (>20 Jahre) können wir daher keine neue Firmware anbieten. \
Ein weiterer Grund ist aber auch, dass diese alten Router das Freifunk Netz stark in der Netzwerk-Geschwindigkeit und bei der Wartung und Entwicklung der Server und Firmware ausbremsen.

Es sind daher einige Router "End-of-Life", andere Router müssen weiterhin auf Openwrt 22 verbleiben,
und die restlichen Router konnten auf Openwrt 25 gehoben werden.

Nebem dem Upgrade auf Openwrt 25, war ein kompletter Umbau der Firewall notwendig (iptables wurde
komplett durch Netfilter ersetzt).

**Hinweise**:
- Da es sich um eine Testing-Version handelt, kann diese noch Fehler enthalten. \
Die Firmware wurde intensiv getestet.
- Die "nightly" Version ist als instabil und unsicher zu betrachten. Das betrifft auch die Sicherheit durch Firewall oder Funktionen, die noch nicht richtig funktionieren. Für normale Nutzer wird von der
"nightly" abgeraten.


## Haupt-Änderungen seit der letzten Release 8.2.7:

- Update auf Openwrt 25.12.0 für ausgewählte Geräte
- Umbau Firewall (iptables -> netfilter)
- LTE Modem Unterstützung verbessert
- Oberfläche: verschiedene Verbesserungen
- Interne Verbesserungen und Optimierungen
- Neue Geräte aufgenommen


## End-Of-Life - keine Firmware mehr verfügbar
Folgende Liste alle Geräte auf, die keine neue Firmware erhalten können.
Diese Geräte sind bereits alter als 20 Jahre und sollten ersetzt werden.

~~~
target: [eol.ath79.22.generic] (22.03)
  Sophos_ap100
  TPLink-tl-wdr3600-v1
  TPLink-tl-wdr4300-v1
  TPLink-tl-wdr7500-v3
  TPLink-tl-wr1043nd-v2
  TPLink-tl-wr1043nd-v3
  TPLink-tl-wr2543-v1

target: [eol.ath79.22.small] (22.03)
  Comfast-cf-e110n-v2
  Comfast-cf-e130n-v2
  Comfast-cf-e314n-v2
  Dlink-dir-825-b1
  netgear_wndr3700
  netgear_wnr2200-8m
  TPLink-archer-c6-v2
  TPLink-cpe210-v1
  TPLink-cpe210-v2
  TPLink-cpe210-v3
  TPLink-cpe220-v2
  TPLink-cpe220-v3
  Ubnt_unifi

target: [eol.sunxi.22.cortexa7] (22.03)
  Xunlong_orangepi-r1

target: [eol.ramips.18.rt305x.tiny] (18.06)
  Dlink-dir-615-d
  Dlink-dir-615-h1

target: [eol.ar71xx.18.generic] (18.06)
  TPLink-tl-wr1043nd-v1
  TPLink-tl-wr842n-v1
  Ubnt-bullet-m
  Ubnt-loco-m-xw
  Ubnt-nano-m-xw
  Ubnt-nano-m

target: [eol.ar71xx.18.tiny] (18.06)
  TPLink-tl-mr3020-v1
  TPLink-tl-mr3220-v1
  TPLink-tl-wa701nd-v2
  TPLink-tl-wa801nd-v1
  TPLink-tl-wa801nd-v2
  TPLink-tl-wa801nd-v3
  TPLink-tl-wa830re-v2
  TPLink-tl-wa850re-v1
  TPLink-tl-wa860re-v1
  TPLink-tl-wa901nd-v2
  TPLink-tl-wa901nd-v3
  TPLink-tl-wa901nd-v4
  TPLink-tl-wa901nd-v5
  TPLink-tl-wr740n-v4
  TPLink-tl-wr741nd-v4
  TPLink-tl-wr840n-v2
  TPLink-tl-wr841-v10
  TPLink-tl-wr841-v11
  TPLink-tl-wr841-v12
  TPLink-tl-wr841-v5
  TPLink-tl-wr841-v7
  TPLink-tl-wr841-v8
  TPLink-tl-wr841-v9
  TPLink-tl-wr940n-v4
  TPLink-tl-wr940n-v6
  TPLink-tl-wr941nd-v2
  TPLink-tl-wr941nd-v5
  TPLink-tl-wr941nd-v6

unused target: [lantiq-xway.22.small] (22.03)
  arcadyan_arv752dpw22
  arcadyan_arv8539pw22

unused target: [lantiq-xrx200.22.small] (22.03)
  tplink_tdw8970

unused target: [ramips.22.mt7620.generic] (22.03)
  tplink_re200-v1

unused target: [ramips.22.mt76x8.generic] (22.03)
  tplink_re200-v2
  tplink_re200-v3
  tplink_re200-v4

unused target: [ath79.22.nand] (22.03)
  netgear_r6100
~~~
