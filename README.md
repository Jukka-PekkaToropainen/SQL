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
 SELECT * FROM opiskelija  "WHERE"WHERE nimi = 999997 

# 8 tehtävä     


#  SELECT * FROM Kurssisuoritus WHERE kurssi = 'pihla'


# 9 tehtävä   

# SELECT * FROM Opiskelija WHERE pääaine LIKE '%a%'
SELECT * FROM opiskelija WHERE "tiede" 

# 10 tehtävä   

# SELECT * FROM opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = 999999 	



 # SELECT Kurssi.nimi Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana FROM Kurssi,kurssisuoritus WHERE Kurssi.Kurssitunnus = kurssisuoritus.kurssi


 # SELECT * FROM Opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija

# Tehtävä 11

# SELECT * FROM Opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija
# Tehtävä 13
# SELECT Tehtävä.nimi AS Tehtävä
   # FROM Kurssi, Kurssitehtävä, Tehtävä, Tehtäväsuoritus
   # WHERE Kurssi.nimi = 'Tietokantojen perusteet'
         AND Kurssi.kurssitunnus = Kurssitehtävä.kurssi
        AND Tehtävä.tunnus = Kurssitehtävä.tehtävä
        AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus;
        WHERE Opiskelija.tehtävät = anna



# 14. 
 Tehtävä: pohdintaa taulujen yhdistämisestä
 toisessa lisätty opiskelija numero


# 15

SELECT opiskelijanumero FROM Opiskelija o 
WHERE o.opiskelijanumero
NOT IN(SELECT opiskelija FROM Kurssisuoritus) 


# 16

# SELECT kurssisuoritus.kurssi AS kurssikoodi, COUNT(*) AS lukumäärä
FROM kurssisuoritus
GROUP BY Kurssikoodi


# 16 
SELECT kurssi.nimi AS kurssi,COUNT(ks.kurssi) as lukumäärä 
FROM Kurssi,kurssisuoritus
WHERE = Kurssi.kurssitunnus
GROUP BY Kurssisuoritus.kurssi



# 17
SELECT kurssi.nimi AS kurssi,COUNT(kurssisuoritus.kurssi) as lukumäärä 
FROM  Kurssi,kurssisuoritus
WHERE  Kurssi.kurssitunnus





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
