# SQL
SQL
# 1. tehtävä matti ja maija nimellä löytyi, omalla ei.
# 2. tehtävä aika moneen varmastikkin....
# 3 tehtävä ![...]TEHTÄVÄ3png.png
# 4 tehtävä SELECT * FROM Kurssisuoritus
# 5 SELECT  kurssi FROM Kurssisuoritus 
 # 6 tehtävä         
#  SELECT DISTINCT kurssi FROM Kurssisuoritus
SELECT * FROM Opiskelija WHERE nimi = 'joni'
 
 # 7  tehtävä       
 # SELECT * FROM Opiskelija WHERE nimi = 'Anna'
 
# 8 tehtävä     

SELECT * FROM Kurssisuoritus WHERE opiskelija = '999999'


# 9 tehtävä   

# SELECT DISTINCT(Pääaine) FROM Opiskelija WHERE pääaine LIKE '%Tiede%' 


# 10 tehtävä   





 # SELECT Kurssi.nimi Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana FROM Kurssi,kurssisuoritus WHERE Kurssi.Kurssitunnus = kurssisuoritus.kurssi


 

# Tehtävä 11

# SELECT Opiskelija.nimi,Kurssi,päivämäärä,arvosana
# FROM Opiskelija, Kurssisuoritus, Kurssi
# WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija
# AND Kurssisuoritus.kurssi = Kurssi.kurssitunnus



# Tehtävä 12

# SELECT kurssi.nimi AS kurssi, tehtävä.nimi AS tehtävä 
# FROM kurssi,tehtävä,kurssitehtävä 
# WHERE tehtävä.tunnus = tehtävä.tunnus
# AND kurssi.kurssitunnus = kurssitehtävä.kurssi

# Tehtävä 13

SELECT kurssi.nimi AS Kurssi. Tehtävä AS Tehtävä
FROM Kurssi,Kurssitehtävä, Tehtävä ,Tehtäväsuoritus ,opiskelija
WHERE Kurssi .kurssitunnus = kurssitehtävä.kurssi 
AND Tehtävä.tunnus =Kurssitehtävä.tehtävä
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus 
AND Opiskelija.opiskelijanumero = Tehtäväsuoritus.opiskelija
AND Opiskelija.nimi = 'Anna'



# 14. 
 Tehtävä: pohdintaa taulujen yhdistämisestä
 toisessa lisätty opiskelija numero


# 15

 # SELECT * FROM Kurssi
 # WHERE Kurssi.Kurssitunnus NOT IN (SELECT kurssi FROM Kurssitehtävä)



# 16

# SELECT kurssisuoritus.kurssi AS kurssikoodi, COUNT(*) AS lukumäärä
FROM kurssisuoritus
GROUP BY Kurssikoodi





# 17

#  SELECT kurssi.nimi AS kurssi, COUNT (*) AS lukumäärä 
FROM Kurssi, Kurssisuoritus  
WHERE kurssi.kurssitunnus = kurssisuoritus.kurssi 
GROUP BY kurssi.nimi


# 18
SELECT k.nimi AS kurssi, COUNT(ks.kurssi) as lukumäärä FROM Kurssi k LEFT JOIN Kurssisuoritus ks
    ON k.kurssitunnus = ks.kurssi GROUP BY k.nimi



# 19
CREATE TABLE Kurssi (kurssitunnus, nimi, kuvaus)

# 20
 INSERT INTO Kurssi (kurssitunnus,  kuvaus, Nimi )
 VALUES ('12345', 'hei maailma', 'SQL-kielen perusteet')
 
# SELECT * FROM Kurssi


# 21
CREATE TABLE Opiskelija
(
    opiskelijanumero integer,
    nimi varchar(200),
    syntymävuosi date,
    pääaine varchar(50)
)

# 21 B
PRAGMA TABLE_INFO(Opiskelija)


# 22 
CREATE TABLE Kurssi
(
    kurssitunnus integer,
    nimi varchar(200),
    kuvaus
  )

# 22 B
PRAGMA TABLE_INFO(Kurssi)

# 23 
opiskelijanumero 
muuttuu joka kerta kun lisää opiskelioita


# 24
CREATE TABLE Kurssi 
(
    kurssitunnus integer PRIMARY KEY,
    nimi varchar(200),
    kuvaus,
    pääaine varchar(50)
)

# 25 PRAGMA foreign_keys = ON;

CREATE TABLE Tehtävä (
    kurssitunnus integer PRIMARY KEY,
    nimi varchar(200) NOT NULL,
    kuvaus varchar(3000)
);

INSERT INTO Kurssi (nimi) VALUES ('Ohpe');
INSERT INTO Kurssi (nimi) VALUES ('Tikape');






# 26 ALTER TABLE Tehtävä ADD COLUMN Tehtävä varchar(50);

# 27 komennolla voi lisätä,poistaa,tai modata taulukkoa.
  voi luoda rajoitteita taulukkoon
  
  
  Esimerkki: ALTER TABLE table_name
ADD column_name datatype; 
ALTER TABLE Customers
ADD Email varchar(255);
