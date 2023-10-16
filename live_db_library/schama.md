# Library Requirements

Sono la libreria dei parioli, abbiamo bisogno di un gestionale per effettuare dei **noleggi** di **libri** ai nostri **utenti**:

- books (libri)
- copies (copie)
- conditions (condizioni) ['buone', 'discrete', 'ottime', 'pessime', 'Da Restaurare']
- genres (generi) ['commedy', 'triller', 'love love']
- loans (noleggi)
- users (utenti)

## table: books

- id | PK, BIGINT, AUTO_INCREMENT, UNIQUE, NOT NULL
- title | VARCHAR(50), NOT NULL
- price | DECIMAL(5, 2), NULL // 999,99
- plot | TEXT, NULL
- vote | FLOAT(2,1), DEFAULT(0) //9.9
- note | TEXT, NULL
- is_available | TINYINT, DEFAULT(0)
- active

## table: copies

- id
- book_id
- condition_id
- cover_image | VARCHAR(255), NULL
- ISBN | CHAR(13), NOT NULL, UNIQUE
- year | YEAR, NULL
- pages | SMALLINT, NULL
- language | VARCHAR(5), NOT NULL
- note | TEXT, NULL
- location | VARCHAR(10), NULL

## table: conditions

- id
- name
- slug

## table: genres

- id
- name
- slug

## table: loans

- id
- user_id
- copy_id
- star_date
- end_date

## table: users

- id
- name
- lastname
- email
  
## Relationships

- books <OneToOne> copies
- books <ManyToMany> genres
- copie <OneToMany> loans
- rents <OneToMany> users
