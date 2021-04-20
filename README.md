# SQL
SQL
# 1. tehtävä matti ja maija nimellä löytyi, omalla ei.
# 2. tehtävä aika moneen varmastikkin....
# 3 tehtävä 
# 4 tehtävä SELECT * FROM Kurssisuoritus
# 5 tehtävä  SELECT Kurssi FROM opiskelija 
 # 6 tehtävä         
 # SELECT * FROM opiskelija " WHERE"  
 
 # 7  tehtävä       
 # SELECT * FROM opiskelija  "WHERE"WHERE nimi = 999997 

# 8 tehtävä     

# SELECT * FROM opiskelija  "WHERE"WHERE nimi


# 9 tehtävä   

# SELECT * FROM opiskelija WHERE "tiede" 

# 10 tehtävä   

# SELECT * FROM opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = 999999 	



 # SELECT Kurssi.nimi Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana FROM Kurssi,kurssisuoritus WHERE Kurssi.Kurssitunnus = kurssisuoritus.kurssi


 # SELECT * FROM Opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija

# Tehtävä 11

# SELECT Opiskelija.nimi AS opiskelija,Kurssi.nimi AS kurssi
# FROM Opiskelija,Kurssisuoritus,Kurssi 
# WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija




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

# SELECT kurssisuoritus.kurssi AS Kurssikoodi COUNT(*) AS lukumäärä
# FROM kurssisuoritus
# GROUP BY Kurssikoodi


