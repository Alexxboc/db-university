<!-- 

Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d'Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni.

 -->


 # DB UNIVERSITY

 ## Departments
    id:                   PRIMARY_KEY  AUTO_INCREMENT         
    name:                 VARCHAR(50)  NOTNULL
    city:                 VARCHAR(58)  NULL

 ## Courses_degrees
    id:                   PRIMARY_KEY  AUTO_INCREMENT   
    name:                 VARCHAR(100) NOTNULL

 ## Subjects
    id:                   PRIMARY_KEY  AUTO_INCREMENT  
    name:                 VARCHAR(100) NOTNULL

 ## Tachers
    id:                   PRIMARY_KEY, AUTO_INCREMENT 
    name:                 VARCHAR(50)  NOTNULL
    last_name:            VARCHAR(50)  NOTNULL
    email:                VARCHAR(50)  NOTNULL 
    phone_number:         VARCHAR(15)  NULL


 ## Exams
    id:                   PRIMARY_KEY, AUTO_INCREMENT 
    name:                 VARCHAR(100) NOTNULL
    year:                 YEAR
    ?mark?:                 

 ## Students
    id:                   PRIMARY_KEY, AUTO_INCREMENT 
    badge_number:         SMALLINT    NOTNULL
    name:                 VARCHAR(50)  NOTNULL
    last_name:            VARCHAR(50)  NOTNULL
    email:                VARCHAR(50)  NOTNULL 
    phone_number:         VARCHAR(15)  NULL
    date_of_birth:        DATE         NULL
    city:                 VARCHAR(58)  NULL



 ## Marks
    id:                   PRIMARY_KEY, AUTO_INCREMENT 
    mark:                 TINYINT      NOTNULL