HOW TO
======

1. Wireguard-Keys manuell erzeugen: 
   `wg genkey > /tmp/private.key`
   `cat /tmp/private.key | wg pubkey > /tmp/public.key`
2. Keepass-Einträge mit diesen Keys für den entsprechenden Host erstellen (z.B. fk-mobil25 public key)
3. Keys in die entsprechenden Hosts Variablen kopieren
4. Keys löschen:
   `rm /tmp/public.key /tmp/private.key`
5. WG-IP-Adresse von der OPNsense WG-Server-Config holen und in der entsprechenden Hosts-Variablen eintragen
6. Peer auf dem Wireguard-Server erstellen und Public-Key einfügen

ATTENTION
=========

Die Sektion `[wireguard-peer.tWgOrYu3YgTJCRG9Qn3Wen6yJTqjCvmiVhGagTEueFQ=]` in homeoffice.nmconnection wird gerade doppelt erzeugt. Die zweite Version überschreibt die erste. Die zweite Version ist korrekt. Ich weiß nicht woher die erste kommt und wie ich sie ändern kann.
