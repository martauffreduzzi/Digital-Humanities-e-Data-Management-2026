# Dati ritratti
#*Tiziano* VS nan

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

 
  
    

    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }


  
    
      
      id
      titolo
      artisti
      data_creazione
      generi
      luoghi
      collezioni
      contenuti
      movimenti
      soggetti
      altezza
      larghezza
    
  
  
    
      0
      http://www.wikidata.org/entity/Q428274
      Ritratto di Fedra Inghirami, detto Fedra
      Raffaello Sanzio (maschio)
      1510
      ritratto
      Galleria Palatina
      Galleria Palatina
      libro; carta; scrittura; strabismo; posizione ...
      Alto Rinascimento
      Tommaso Inghirami
      91.0
      61.0
    
    
      1
      http://www.wikidata.org/entity/Q151047
      Nascita di Venere
      Sandro Botticelli (maschio)
      1485
      nudo artistico; pittura mitologica
      NaN
      Palazzo degli Uffizi
      mare; donna; cielo; vento; albero; Afrodite; c...
      Rinascimento; Primo Rinascimento
      Venere Anadiomene; nascita di Afrodite
      172.5
      278.5
    
    
      2
      http://www.wikidata.org/entity/Q180632
      Ritratto di Paolo III con i nipoti Alessandro ...
      Tiziano Vecellio (maschio)
      1546
      ritratto; ritratto di gruppo
      Museo nazionale di Capodimonte
      Museo nazionale di Capodimonte
      tavolo; tenda; papa Paolo III; Ottavio Farnese...
      manierismo; pittura veneta
      papa Paolo III
      210.0
      176.0
    
    
      3
      http://www.wikidata.org/entity/Q368788
      Pietà
      Perugino (maschio)
      1483
      arte religiosa
      Palazzo degli Uffizi
      Palazzo degli Uffizi
      Gesù; donna; Maria; uomo
      rinascimento italiano
      Pietà
      168.0
      176.0
    
    
      4
      http://www.wikidata.org/entity/Q549847
      Primavera
      Sandro Botticelli (maschio)
      1480
      allegoria; pittura mitologica
      Palazzo Medici Riccardi; Galleria delle pittur...
      Palazzo degli Uffizi
      mela; donna; fiore; Mercurio; primavera; Cupid...
      Primo Rinascimento
      primavera
      207.0
      319.0
    
  


    

  
    

  
    
  
    

  
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  

    
      const buttonEl =
        document.querySelector('#df-08bdf6a0-e2ae-4e2a-b8e5-a4379ef401b8 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-08bdf6a0-e2ae-4e2a-b8e5-a4379ef401b8');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    
  


    
  


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

