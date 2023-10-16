# DB First

Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## Model

- Car

## Table

- cars

## cars table

- id | BIGINT, PK, AI, NOT NULL, UNIQUE
- brand | VARCHAT(50), NOT NULL, INDEX
- model | VARCHAR(50), NOT NUL, INDEX
- cover_image | VARCHAT(255), NULL
- year | YEAR, NOT NULL, INDEX
- color | VARCAR(10), NULL
- doors | TINYINT | NULL
- seats | TINYINT | NULL
- drive_side | DEFAULT('left')
- transmission_type | VARCHAR(15), NOT NULL, INDEX
- horsepower | VARCHAR(20), NULL
- cc | VARCHAR(10), NULL
- price | DECIMAL(8, 2), NULL
- vin | CHAT(17), NULL, UNIQUE
- engine_type | VARCHAR(15), NULL
- plate_number | VARCHAR(10), NULL, UNIQUE
- km | MEDIUMINT(), NULL
- is_new | TINYINT(), DEFAUL(0)
- is_available | TINYINT, DEFAULT(0)
- description | TEXT, NULL
- note | TEXT, NULL
