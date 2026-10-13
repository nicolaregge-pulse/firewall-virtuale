# firewall-virtuale

Progetto di stage: **imparare a configurare un router-firewall** senza avere un dispositivo vero.

Il simulatore è una pagina web: un router virtuale ispirato ai router MikroTik, che si configura in due modi, come quelli veri:

1. **con le finestre e i bottoni**, come nel programma Winbox;
2. **con il terminale**, con un linguaggio semplificato preso da RouterOS.

Accanto c'è una piccola rete simulata (PC, server, Internet): si manda un pacchetto e si vede se passa o viene bloccato, e da quale regola.

## Come si lavora

1. Il percorso, livello per livello: `documenti/PERCORSO.md`.
2. La chat del progetto: la Pull Request «Chat del progetto (e diario)». Lì si fanno le domande; il prof e Claude rispondono.
3. Il diario, giorno per giorno: la cartella `storia/`.
4. Le configurazioni salvate a ogni livello: la cartella `configurazioni/`.

## Attenzione

È una simulazione didattica: insegna i concetti (interfacce, indirizzi IP, routing, NAT, regole del firewall) e la logica dei comandi. Non è il software di MikroTik e non tutti i comandi si comportano come su un dispositivo reale.
