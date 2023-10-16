# Library Database

## Table name

- books

## Table columns

- id | PK, BIGINT, AUTO_INCREMENT, UNIQUE, NOT NULL
- title | VARCHAR(50), NOT NULL
- ISBN | CHAR(13), NOT NULL, UNIQUE
- year | YEAR, NULL
- pages | SMALLINT, NULL
- price | DECIMAL(5, 2), NULL // 999,99
- plot | TEXT, NULL
- vote | FLOAT(2,1), DEFAULT(0) //9.9
- language | VARCHAR(5), NOT NULL
- cover_image | VARCHAR(255), NULL
- note | TEXT, NULL
- is_available | TINYINT, DEFAULT(0)
- location | VARCHAR(10), NULL
- active

<!-- Non vanno nella tabella books -->
- author (not here - not like that)
- genre (not here - not like that)
- target (not here)
- edition (not here - not like that)
- format (not here - not like that)
- publisher (not here)
- condition (not here)
