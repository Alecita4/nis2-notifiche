Azienda:
NuvolaPMI S.r.l.: piccolo provider italiano che offre servizi cloud a circa 1.200 piccole e medie imprese.

Servizi critici:
Codice	Servizio	Utenti totali (esempio)
S1	Hosting di siti web ed e-commerce	1.200 clienti
S2	Posta elettronica aziendale	6.000 caselle
S3	Backup in cloud	800 clienti

Fonte delle soglie:

Per i provider cloud esiste un regolamento europeo che dice già quando un incidente è significativo: il Regolamento di esecuzione (UE) 2024/2690, articolo 7. Il regolamento è vincolante e direttamente applicabile in tutti gli Stati membri dal 7 novembre 2024.


L’articolo 7 dice, in sostanza, che l’incidente è significativo se:

un servizio cloud è completamente indisponibile per più di 30 minuti;

la disponibilità di un servizio cloud è limitata per più del 5% degli utenti nell’Unione, o per più di 1 milione di utenti, a seconda di quale numero è più basso, e questo dura più di un’ora;

l’integrità, la riservatezza o l’autenticità dei dati conservati, trasmessi o elaborati è compromessa con un impatto su più del 5% degli utenti.

Regole:

ID	Regola	                                                                                        Grandezze usate
R1	SE minuti_indisponibilita_totale > 30 ALLORA significativo	durata
R2	SE percentuale_utenti_con_servizio_degradato > 5 E minuti_degrado > 60 ALLORA significativo	utenti impattati + durata
R3	SE dati_compromessi = SI E percentuale_utenti_con_dati_compromessi > 5 ALLORA significativo	categorie di dati + utenti