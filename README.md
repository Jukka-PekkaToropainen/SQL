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

# SELECT o.nimi opiskelija, k.arvosana
    FROM Opiskelija o, Kurssisuoritus k
    WHERE o.opiskelijanumero = k.opiskelija
NOT IN (SELECT opiskelija FROM Kurssisuoritus)



# 16

# SELECT kurssisuoritus.kurssi AS kurssikoodi, COUNT(*) AS lukumäärä
FROM kurssisuoritus
GROUP BY Kurssikoodi





# 17

SELECT k.nimi AS kurssi, ks.arvosana AS arvosana, COUNT (ks.opiskelija) AS lukumäärä
    FROM Kurssi k, Kurssisuoritus ks WHERE k.kurssitunnus = ks.kurssi
        GROUP BY k.nimi, ks.arvosana



# 18
SELECT k.nimi AS kurssi, COUNT(ks.kurssi) as lukumäärä FROM Kurssi k LEFT JOIN Kurssisuoritus ks
    ON k.kurssitunnus = ks.kurssi GROUP BY k.nimi



# 19
CREATE TABLE Kurssi (Kurssi, kurssitunnus, nimi, kuvaus)

# 20
 INSERT INTO Kurssi (kurssitunnus,  kuvaus, Kurssi )
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
