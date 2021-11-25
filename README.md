# Act. Aval.: 25 de novembre 2012
## **MP02**: Base de Dades - **UF02**: Llenguatges SQL: DML i DDL

<br>

## **Requeriments**
<hr>

Aquesta activitat cal fer-la en local al vostre ordinador, i fent servir la **màquina virtual** que fem servir a classe, i a on teniu instal·lat el **```docker```** i un **contenidor** amb **```mysql```** creat.

Recordatori de les comandes per crear el contenidor, si no el teniu ja creat.
> *```sudo docker run --name ```*  **```<nomContenidor>```** *```-e MYSQL_ROOT_PASSWORD=12345 -d  mysql:latest```*
> <br><br>

 a on **```<nomContenidor>```** és el nom del vostre contenidor.

Comanda per accedir al contenidor:
>&nbsp;&nbsp;*```$```* **```sudo docker exec -ti jpc-mysql bash```** 
>
>&nbsp;&nbsp;*```root@25eb09e8df2c:/#```*&nbsp;&nbsp;&nbsp;**```mysql -u root -p```**
>
>&nbsp;&nbsp;```Enter password:``` &nbsp;&nbsp;*12345*
>
>&nbsp;&nbsp;```Welcome to the MySQL monitor.  Commands end with ; or \g.``` 
>
>&nbsp;&nbsp;```Your MySQL connection id is 46``` 
>
>&nbsp;&nbsp;```Server version: 8.0.27 MySQL Community Server - GPL``` 
>
>&nbsp;&nbsp;```Copyright (c) 2000, 2021, Oracle and/or its affiliates.``` 
>
>&nbsp;&nbsp;```Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.```
>
>&nbsp;&nbsp;```Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.```
>
>&nbsp;&nbsp;```mysql> ```

<br>

## **Pasos previs**
<hr>

1. Abans de començar, cal que cloneu el **repositori remot** de l'activitat a un **repositori local** al vostre ordinador.

    >  **```$ sudo git clone https://github.com/joanpardogine/DAW_MP02_020_UF02_Act_Ava_20211125.git```**


1. Recordeu que la comanda ***```clone```*** us ha creat un enllaç anomenat ***```origin```***,

1. Ho podeu comprobar executant la comanda:

    >  **```$ git remote get-url origin ```**
    >  **```https://github.com/joanpardogine/DAW_MP02_020_UF02_Act_Ava_20211125.git```**

1. Per després no tenir problemes, cal que elimineu l'enllaç anomenat ***```origin```*** que teniu creat, abans de continuar.

    >  **```$ git remote remove origin ```**

1. Podeu comprobar que ja no en teniu cap enllaç, executant la comanda:

    >  **```$ git remote ```**
    >
    >  **```$```**

    Si no apareix res, vol dir que no hi ha cap enllaç. És a dir, és el que ha de ser, que no hi ha cap enllaç.

1. A continuació, cal que creeu un **repositori remot** al vostre compte de **```github.com```**, amb els següents detalls:
    1. Amb el **nom** del **repositori remot**:

        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;***```<CognomAlumne><NomAlumne>```*```_ActAva_20211125```**
    1. El **repositori remot** cal que sigui de tipus ***```privat```***.
    1. Cal que convideu a l'usuari ***```joanpardogine```***

1. Un cop creat el vostre **repositori remot**, cal que el vinculeu amb el vostre **repositori local**. Per tant, cal seguir els passos de sempre.
    * Des d'una finestra terminal del **visual studio code**, executeu les següents comandes.
    > $ ``` git remote add origin https://github.com/<```  ***nomUsuariDeGithub***```>/<```***CognomAlumne***```><```***NomAlumne***```>_ActAva_20211125.git```

1. Ho podeu comprobar executant la comanda:
    >  $ ``` git remote get-url origin ```**
    >
    >  ```https://github.com/<```  ***nomUsuariDeGithub***```>/<```***CognomAlumne***```><```***NomAlumne***```>_ActAva_20211125.git```


<br>

### Arribats a aquest punt, ja podeu **començar**. 

1. Per que quedi constancia de què ja heu començat l'activitat cal que executis un **```commit```** i que el pujis al teu **repositori remot**.

1. És a dir, que cal que executis les següents comandes:
    >  $ ``` git add . ```
    >
    >  $ ``` git commit -m "Comença l'activitat!"```
    >
    >  $ ``` git push -u origin main```
    >

1. Per pujar la resolució de cada apartat, caldrà que puguis al teu **repositori remot** un fitxer amb extensió **```.sql```** a on aparegeui la teva solució a cada apartat. Caldrà un fitxer per apartat.

    > Recorda que per avaluar la teva activitat, copiaré el continngut íntegre del teu fitxer. Per tant, cal que t'asseguris de que hi haurà cap error quan l'executi al meu servidor. 

1. Cada fitxer caldrà que tingui el següent nom:
    > <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```&lt;***XX***&gt;```.sql```

     a on &lt;***XX***&gt; és el número de l'enunciat que responeu.

1. I per últim, **però no menys important**, per que quedi constancia de què aneu avançant, després de cada enunciat cal que feu un **```commit```** i que el pugeu el fitxer amb la vostra resposta al vostre **repositori remot**. És a dir, que cal que executeu les següents comandes:

    >  $ ``` git add . ```
    >
    >  $ ``` git commit -m "Fet i pujat l'enunciat ``` &lt;***XX***&gt;```!"```
    >
    >  $ ``` git push -u origin main```
    >
    a on &lt;***XX***&gt; és el número de l'enunciat que responeu.

<br>
<hr>
<br>

## A partir del següent **MER**:
![MER](./ActAva_20211125_MER.png)


En el següent fitxer  [**```ActAva_20211125.sql```**](./ActAva_20211125.sql), trobaràs tota la informació per crear i omplir de la base de dades.

Cal que vagis responent el que es demana als següents apartats.

 <br>
 <hr>

## **Enunciat 1**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(0.5 punts)
>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```01```****```.sql```*

* Mostra un llistat a on aparegui el **```nom del producte```**, les **```unitats per producte```** i el **```preu del producte```** de tots els productes que pertanyen a la categoria amb codi **```5```**. (***No** cal mostrar el nom de la categoria.*)
 
 <br>
 <hr>

## **Enunciat 2**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(0.5 punts)
>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```02```****```.sql```*

* Mostra un llistat a on aparegui el **```nom del producte```**, el **```nom del proveïdor```** i el **```nom de la categoria```**,  de tots els **productes**.

 <br>
 <hr>

## **Enunciat 3**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(0,5 punts)
>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```03```****```.sql```*

* Mostra un llistat a on aparegui el **```nom del producte```**, el **```nom del proveïdor```** i el **```nom de la categoria```**, i que estigui ***ordenat*** per **categoria**.

 <br>
 <hr>

## **Enunciat 4**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1 punt)
>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```04```****```.sql```*

* Mostra un llistat a on aparegui el **```nom del producte```**, el **```nom del proveïdor```** i la **quantitat de productes** (**suma** *de productes*) que tenim de cada **```proveïdor```**.


 <br>
 <hr>


## **Enunciat 5**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1 punt)
>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```05```****```.sql```*

* Mostrar el **```nom del treballador```**, el **```cognom del treballador```** i l'**```edat del treballador```** de tots els treballadors. A les columnes cal que apareguin els següents títols: **Nom**, **Cognom** i **Edat del trebalador**.


 <br>
 <hr>


## **Enunciat 6**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(0.5 punts)
>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```06```****```.sql```*

* Mostrar el **```nom del treballador```**, el **```cognom del treballador```** i l'**```edat del treballador```** de tots els treballadors. A les columnes cal que apareguin els següents títols: **Nom**, **Cognom** i **Edat del trebalador**, i cal que el llistat estigui **ordenat** per l'**```edat del treballador```**.


 <br>
 <hr>

## **Enunciat 7**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1 punt)

>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```07```****```.sql```*

* Mostra el **nom del client** i la **quantitat de comandes** que ha realitzat el client de **Barcelona**. Cal que facis la consulta amb una subconsulta.

 <br>
 <hr>


## **Enunciat 8**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1 punt)

>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```08```****```.sql```*

* Mostra el **nom del client** i la **quantitat de comandes** que ha realitzat el client que té el **máxim** de comandes. Cal que facis la consulta amb una subconsulta.

 <br>
 <hr>


## **Enunciat 9**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2 punt)

>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```09```****```.sql```*

* Mostrar els treballadors (**nom** i **cognom**) acompanyats del **```nombre de comandes```** que han gestionat, **ordenats** pel **cognom**.
<br>
 <hr>

## **Enunciat 10**:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2 punt)

>  <***```CognomAlumne```***><***```NomAlumne```***>```_ActAva_20211125_Enunciat```***```10```****```.sql```*

* Mostrar el rànquing dels treballadors (**nom** i **cognom**), segons el nombre de comandes que han gestionat, que n’hagin gestionat més de cinc.
<br>
 <hr>