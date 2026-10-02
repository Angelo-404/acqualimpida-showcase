# AcquaLimpida

Il codice di questo progetto è privato. Qui racconto cosa fa, come è costruito e come l'ho verificato.

## Cosa fa

È una piattaforma per chi fa manutenzione di piscine, per privati e aziende. Il tecnico registra interventi e
analisi dell'acqua anche dove non c'è campo, e il cliente ha un suo portale dove vede lo storico della sua piscina.
Più aziende di manutenzione possono usarla insieme, ognuna con i propri dati separati.

## Come è costruito

React e Vite per un'app installabile che funziona offline. Supabase con PostgreSQL per i dati, con regole di accesso
riga per riga (RLS) e funzioni lato server. Il calcolo della chimica dell'acqua è un modulo separato, senza
dipendenze, che si può provare da solo.

## Come l'ho verificato

96 test automatici sui permessi, eseguiti contro il database vero: verificano che ogni ruolo veda solo i dati della
propria azienda e dei propri clienti.

## Stato

In pausa.
