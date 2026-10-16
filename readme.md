# Analisi dell’associazione tra rating a stelle e volume di acquisti recenti su Amazon

## Obiettivo
Quantificare l’associazione tra il rating medio a stelle e il volume di acquisti recenti riportato per prodotti Amazon, utilizzando un dataset pubblico di listing.

## Dataset
- File: `amazon_sales_data_uncleaned.csv`
- Origine: raccolta di listing Amazon (principalmente categoria elettronica)
- Campi principali utilizzati: Title, Rating, Number_of_reviews, bought_in_last_month

## Metodologia
1. Estrazione dei valori numerici da campi testuali (rating e volume di acquisti).
2. Filtraggio dei record con rating e volume di acquisti validi.
3. Calcolo della correlazione di Pearson tra rating e volume di acquisti recenti.
4. Aggregazione del volume medio di acquisti per fasce di rating.
5. Visualizzazione della relazione tramite scatter plot (scala logaritmica sull’asse y).
6. Estrazione dei 10 prodotti con volume di acquisti più elevato.

## Strumenti
Python, pandas, matplotlib, seaborn.

## Risultati
- Record analizzati: 32.140
- Correlazione di Pearson (rating vs acquisti recenti): 0.073
- Volume medio di acquisti recenti per fascia di rating:
  - < 4.0: 488
  - 4.0 – 4.5: 510
  - ≥ 4.5: 2.544
- I prodotti con rating ≥ 4.5 registrano un volume medio di acquisti recenti circa 5 volte superiore rispetto alle fasce inferiori.

## Osservazioni
I dati mostrano un’associazione positiva tra rating a stelle e volume di acquisti recenti.  
I prodotti con rating ≥ 4.5 presentano un volume medio di acquisti significativamente più elevato (circa 5x) rispetto ai prodotti con rating inferiore a 4.5.  
Il rating rappresenta un segnale visibile associato a un volume di vendita recente più alto.

## Limiti
- I dati si riferiscono a un singolo periodo di raccolta.
- Il campo “bought in past month” è un valore approssimato riportato dalla piattaforma.
- Non sono controllate variabili come prezzo, marca, posizione in pagina o promozione.

## Esecuzione
Il notebook contiene le fasi di caricamento, pulizia, analisi e visualizzazione in sequenza.