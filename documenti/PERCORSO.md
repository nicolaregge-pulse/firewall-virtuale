# Il percorso: configurare un router-firewall

**Versione 1.0** — 13/10/2026 — Laboratorio di Informatica, prof. Nicola Regge, Piamarta Milano.

Il simulatore è nel browser: nessuna installazione. Ogni missione ha un obiettivo; il simulatore controlla da solo quando è fatta. A ogni missione: salvi l'export in `configurazioni/` con un commit e sai rispondere alla domanda a voce, con parole tue.

Le domande si fanno nella chat del progetto (Pull Request «Chat del progetto»). Il prof e Claude rispondono lì.

## Le parole

| Parola | Che cosa vuol dire |
|---|---|
| Interfaccia (ether1, ether2…) | una porta del router, dove si attacca un cavo |
| WAN e LAN | il lato verso Internet (WAN) e la rete interna (LAN) |
| Indirizzo e maschera (192.168.88.1/24) | l'indirizzo della porta e quanto è grande la sua rete (/24 = 256 indirizzi) |
| Gateway | la «porta d'uscita» a cui un computer manda i pacchetti per le reti che non conosce |
| Rotta predefinita (0.0.0.0/0) | «tutto quello che non conosci, mandalo lì» |
| NAT masquerade | il router cambia il mittente privato con il suo indirizzo pubblico, così le risposte tornano |
| Firewall, catene | input = pacchetti per il router stesso; forward = pacchetti che attraversano il router |
| Regola | se il pacchetto corrisponde, si fa l'azione (accept, drop, reject); vale la prima dall'alto |
| dst-nat (inoltro di porta) | chi arriva da Internet su una porta viene mandato a un computer interno |

## Le missioni

| N. | Obiettivo | Sai spiegarlo? |
|---|---|---|
| 1 | Dai l'indirizzo 192.168.88.1/24 alla porta ether2 | Perché i PC hanno bisogno del gateway? |
| 2 | Collegati a Internet: 203.0.113.2/30 su ether1 e la rotta 0.0.0.0/0 verso 203.0.113.1 | Che cosa fa la rotta predefinita? |
| 3 | Fai navigare la rete interna con il NAT (masquerade) | Perché senza NAT la risposta non torna? |
| 4 | Blocca il PC 2 verso Internet, ma non verso il server interno | Perché la regola va nella catena forward? |
| 5 | Proteggi il router da Internet (SSH, Winbox) | Che differenza c'è tra input e forward? |
| 6 | Pubblica il server web con il dst-nat, porta 80 | Che cosa succede alla destinazione del pacchetto? |

## Dopo le missioni

1. **Fallo tuo:** dai il tuo nome al router (`/system identity set name=...`).
2. **Le regole dell'ordine:** metti una regola «accept» sopra una «drop» e guarda che cosa cambia (`move`).
3. **Il confronto con il vero:** con l'export in mano, cerca nella documentazione di MikroTik gli stessi comandi e annota le differenze.
4. **Prossime versioni del simulatore** (le chiedi tu nella chat): DHCP, una seconda rete (ospiti), regole con lo stato della connessione (established), il log dei pacchetti bloccati.

## Registro delle versioni

1. **v1.0 (13/10/2026):** prima versione: sei missioni.
