## dipartimenti

- id | TINYINT PK UQ NN
- name | VARCHAR(40) NN

## corsiLaurea

- id | TINYINT PK UQ NN
- dipartimento_id
- name |VARCHAR(40) NN
- tot_credits | TINYINT

## corsi

- id | SMALLINT PK UQ NN
- credits | TINYINT

## appelli

- id | INT PK UQ NN
- corso_id
- datetime | DATETIME
- room | VARCHAR(20)

## corsoLaurea_corso (pivot)

- id | INT PK UQ NN
- corsoLaurea_id
- corso_id
- obbligatorio |TINYINT N DEFAULT(0)

## professors

- id | INT PK UQ NN
- name | VARCHAR (30)
- lastname | VARCHAR (30)
- email | VARCHAR (30)
- officeLocation | VARCHAR (30)
- cv | MEDIUMTEXT

## professor_corso (pivot)

- corso_id
- professor_id

## students

- matricola | VARCHAR (20) PK UQ NN
- corsoLaurea_id
- name | VARCHAR (30)
- lastname | VARCHAR (30)

## student_appello (pivot)

- id | BIGINT PK UQ NN AI
- appello_id
- student_id
- hasAttended |TINYINT N DEFAULT(0)
- result | TINYINT N
