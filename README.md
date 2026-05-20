# Dati 'ritratti' : *Tiziano* VS **NaN** 

## Descrizione
Questo progetto analizza un dataset storico-artistico contenente dati su 2444 opere d'arte, organizzati in 12 variabili. 

| Colonna         | Valore                                  |
|:----------------|:----------------------------------------|
| id              | http://www.wikidata.org/entity/q428274  |
| titolo          | ritratto di fedra inghirami, detto fedra |
| artisti         | raffaello sanzio (maschio)              |
| generi          | ritratto                                |
| luoghi          | galleria palatina                       |
| collezioni      | galleria palatina                       |
| contenuti       | libro; carta; scrittura; strabismo; posizione... |
| movimenti       | alto rinascimento                       |
| soggetti        | tommaso inghirami                       |
| altezza         | 91.0                                    |
| larghezza       | 61.0                                    |
| years           | 1510.0                                  |

 


A seguito di una prima analisi e pulizia dati, sono emerse curiosità che sono state poi indagate attraverso manipolazione ed estrazione dati. Una ricerca incrociata tra generi e picchi cronologici ha evidenziato anomalie dovute presumibilmente alla catalogazione dei dati in input. Ci si è poi concentrati sul genere 'ritratto' per estrarne l'artista più prolifico. Tiziano risulta essere, nel dataframe preso in considerazione, il ritrattista più prolifico dal 1086 al 2016. Questo dato, in correlazione a un valore nullo piuttostosto significativo, ha sollevato altre domande. Combinando i dati estratti da tale ricerca e le conoscenze storico-artistiche pregresse si è scelto di indagare meglio su eventuali mancanze del dataframe. Sono emerse importanti lacune di dati.

## Fonti
Il dataset utilizzato è stato precedentemente fornito durante il corso *Digital Humanities e Data Management* dell'Università di Bologna, tramite seguente link [https://raw.githubusercontent.com/dhdmch/2025-2026/refs/heads/main/data/vapod/data.csv](https://raw.githubusercontent.com/dhdmch/2025-2026/refs/heads/main/data/vapod/data.csv)

## Metodi e strumenti
Il progetto è stato sviluppato in ambiente *Google Colab*, utilizzando il linguaggio di programmazione *Python*, con l'aiuto di *Google Gemini*. Sono state poi importate le librerie *Pandas* e *Matplotlib* per la manipolazione e la visualizzazione dei dati.

## Responsabili
Marta Uffreduzzi

## Licenza
Il progetto è stato rilasciato sotto **Licenza CC0 1.0 Universal**.
[https://creativecommons.org/publicdomain/zero/1.0/](https://https://creativecommons.org/publicdomain/zero/1.0/)

