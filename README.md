## Modellare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## DB_NAME : *car_dealer*
- Table Name : ***Car***

1. ID Auto : INDEX | BIGINT | PK | NOTNULL | UNIQUE | AI 
2. Marca : VARCHAR (20) | NULL
3. Modello : INDEX | VARCHAR(80) | NOTNULL | DEFAULT ('N/A')
4. Anno di produzione : YEAR | NULL
5. Chilometraggio : MEDIUMINT | NULL
6. Prezzo : DECIMAL(10,2) | NOTNULL 
7. Colore : VARCHAR(30) | NULL
8. Tipo di carrozzeria : VARCHAR(30) | NULL
9. Tipo di carburante : VARCHAR(30) | NULL
10. Descrizione : TEXT | NULL
<!-- TwoChoices : -->
11a. Stato : ENUM('Disponibile', 'Venduta') | NOT NULL | DEFAULT ('Info non valida')
11b. Disponibilità : TINYINT <!-- TRUE or FALSE --> | NOT NULL
<!-- /TwoChoices : -->
12. Data di inserimento : DATETIME | NOT NULL
13. Data di vendita : DATETIME | NULL

              | |
              | |
              | |
            \     /
             \   /
              \ /
               V 

| Campo                | Descrizione                                                                    |
|----------------------|-----------------------------------------------------------------------------   |
| ID Auto (PK)         | Identificatore univoco dell'auto                                                |    
| Marca                | Marchio dell'auto (es. Toyota, Ford, etc.)                                     |
| Modello              | Modello dell'auto (es. Corolla, Mustang, etc.)                                 |
| Anno di produzione   | Anno di produzione dell'auto                                                   |
| Chilometraggio       | Chilometraggio dell'auto                                                       |
| Prezzo               | Prezzo di vendita dell'auto                                                    |
| Colore               | Colore dell'auto                                                               |
| Tipo di carrozzeria  | Tipo di carrozzeria dell'auto (Berlina, SUV, coupé, ecc.)                      |
| Tipo di carburante   | Tipo di carburante dell'auto (Benzina, Diesel, ibrido, elettrico, ecc.)        |
| Descrizione          | Breve descrizione dell'auto e delle sue caratteristiche                        |
| Stato/Disponibilità  | Stato dell'auto (Disponibile, Venduta)                                         |
| Data di inserimento  | Data in cui l'auto è stata inserita nel database                               |
| Data di vendita      | Data in cui l'auto è stata venduta (se applicabile)                            |

