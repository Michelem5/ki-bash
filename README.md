# ki-bash

ki - KI-Terminal-Assistent (lokal oder Remote via Ollama)

Verwendung:
  ki [OPTIONEN] "Frage"
  echo "Ausgabe" | ki [OPTIONEN] "Frage"
  ki -s "Frage" | bash
  ki install | update | server | uninstall | chat

Optionen:
  -s  Short: Gibt nur den Shell-Befehl zurück
  -c  Startet interaktiven Chatverlauf
  -h  Zeigt diese Hilfe an

Parameter:
  install    Ollama + Modell lokal installieren; mit KI_LAN nur Remote-IP hinterlegen
  update     Aktualisiert das Skript via GitHub (Michelem5/ki-bash)
  server     Wie install, setzt zusätzlich OLLAMA_HOST=0.0.0.0 (LAN-Zugriff)
  uninstall  Deinstalliert Ollama und/oder das Skript (mit Bestätigung)
  chat       Startet interaktiven Chatverlauf (Beenden: exit | /bye | tschüss | ade | Ctrl+C)

Umgebungsvariable:
  KI_LAN="192.168.1.53"   Remote-Ollama-IP (leer = Default oder 127.0.0.1)
  KI_MODEL="modellname"   Erzwingt ein bestimmtes Modell

Beispiele:
  ki chat; ki -c
  ki install
  KI_LAN=192.168.1.2 ki install
  ki "Erkläre systemd journalctl"
  ki -s "Wie sehe ich alle offenen Ports"
  echo "ss -tulpen" | ki "Erkläre die Ausgabe"
  cat text.txt | ki -c "was stimmt damit nicht?"
  cat text.txt | ki chat "was stimmt damit nicht?"
