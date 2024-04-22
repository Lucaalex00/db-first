## Modellare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## DB_NAME : *car_dealer*
- Table Name : ***Car***


1. ID Auto (Primary Key): Un identificatore univoco per ogni auto inserita nel database.
2. Marca: Il marchio dell'auto (es. Toyota, Ford, etc.).
3. Modello: Il modello dell'auto (es. Corolla, Mustang, etc.).
4. Anno di produzione: L'anno di produzione dell'auto.
5. Chilometraggio: Il chilometraggio dell'auto.
6. Prezzo: Il prezzo di vendita dell'auto.
7. Colore: Il colore dell'auto.
8. Tipo di carrozzeria: Berlina, SUV, coupé, ecc.
9. Tipo di carburante: Benzina, Diesel, ibrido, elettrico, ecc.
10. Descrizione: Una breve descrizione dell'auto e delle sue caratteristiche.
11. Stato: Indica se l'auto è disponibile o già venduta.
12. Data di inserimento: Data in cui l'auto è stata inserita nel database.
13. Data di vendita: Data in cui l'auto è stata venduta (se applicabile).
<!-- 14. ID Concessionario  (Foreign Key): Un riferimento all'ID del concessionario che ha inserito l'auto. -->

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