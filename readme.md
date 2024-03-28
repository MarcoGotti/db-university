## dipartimenti

- id | TINYINT PK UQ NN
- name | VARCHAR(40) NN

## corsiLaurea

- id | TINYINT PK UQ NN
- dipartimento_id
- name |VARCHAR(40) NN
- tot_credits | TINYINT

## corsi

- id | TINYINT PK UQ NN
- credits | TINYINT

## appelli

- id | INT PK UQ NN
- corso_id
- date | DATETIME
- room | VARCHAR(20)

## corsoLaurea_corso (pivot)

- corsoLaurea_id
- corso_id
- ?obbligatorio BOOL

## professors

- id | INT PK UQ NN
- name | VARCHAR (30)
- lastname | VARCHAR (30)

## professor_corso (pivot)

- corso_id
- professor_id

## students

- id | BIGINT PK UQ NN
- corsoLaurea_id
- appello_id
- name | VARCHAR (30)
- lastname | VARCHAR (30)
