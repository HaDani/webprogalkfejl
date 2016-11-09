# webprog-beadando

A választott beadandó feladat:

<h1>TO-DO alkalmazás fejlesztése</h1>

<h2>Funkcionális követelmények:</h2>
A beadandó program célja az adatbázisba felvitt feladatok/tennivalók megjelenítése, valamint azok megjelölése elvégzettként, törlése.   

Felhasználóként szeretnék elvégzendő feladatot/tennivalót hozzáadni -> Feladat hozzáadása <br>
Felhasználóként szeretném megjelelölni az elvégzett feladatokat, vagy törölni azokat. -> Feladat törlése <br>
Felhasználóként szeretném tudni csoportosítani a feladataimat -> Feladatok csoportosítása <br>
Felhasználóként szeretném, ha az alkalmazás listázná a legkorábban feltöltött és még nem elvégzett feladataimat -> Feladatok megtekintése <br>

A felhasználó bejelentkezés után:
 - Tennivalót adhat hozzá a listájához
 - Tennivalót törölhet, jelölhet meg elvégzettként, vagy jelölheti meg magas prioritásuként
 - Megtekintheti a hozzáadott feladatait, valamint módosíthatja azokat

Amennyiben a felhasználó még nem jelentkezett be, úgy az oldalon megjelenik egy ismertető, amely leírja az alkalmazás fontosabb funkciót,
valamint azok működését

<h2>Nem funkcionális követelmények:</h2>
<ul>
<li>Felhasználóbarát, modern megjelenés</li>
<li>Gyors működés</li>
<li>Biztonságos működés</li>
</ul>

<h2> Szakterületi fogalomjegyzék: </h2>
<b> ToDo: </b> Az elvégzendő tevékenység leírásá szolgál.

<h2> Használatieset-modell, funkcionális követelmények </h2>

<b> Vendég: </b> 
<ul>
 <li> Az oldalt megtekintheti, azonban mivel a funkciók csak bejelentkezés után érhetőek el, így nem tud ToDo-t létrehozni, módosítani </li>
 <li> Regisztráció </li>
 <li> Bejelentkezés </li>
 </ul>
 
 <b> Bejelentkezett felhasználó: </b>
 <ul>
 <li> A publikus oldalakon kívül hozzáfér további opciókhoz is. </li>
 <li> ToDo létrehozása </li>
 <li> ToDo-k megtekintése </li>
 <li> ToDo módosítása </li>
 <li> ToDo megjelölése elvégzettként </li>

![Használatieset-modell](docs/nomnoml.png)

 <h2> ToDo módosítása </h2>
 <ol>
 <li> Az oldalra érkezett vendég regisztrál, vagy bejelentkezik </li>
 <li> Amennyiben már regisztrált és adott hozzá tevékenységet, úgy a következőket teheti: </li>
 <ul> 
  <li> Megtekintheti az eddig hozzáadott ToDo-jait
  <li> A ToDo neve melletti módosít gombra kattintva módosíthatja azt
  <li> A ToDo neve melletti kész gombra kattintva elvégzettnek tekintheti az adott tevékenységet, mely ezáltal törlésre kerül
 </ul>
 <li> Amennyiben a módosít gombra kattintott úgy megjelenik számára a módosító felület, melyen átírhatja a ToDo nevét, leírását, valamint megváltoztathatja annak kategóriáját.
 <li> Az új adatok bevitele után az elküld gombra kattintva a ToDo módosításai mentésre kerülnek
 </ol>
 </ul>
 </ol>
 
 ![ToDo módosítása diagram](docs/modifyToDo.png)


<h1>
Tervezés
</h1>

<h2>
Architektúra modell
</h2>

<h3> Komponens diagram </h3>

![Komponens diagram](docs/dbmodell.png)


<h2>
Oldaltérkép </h2>

<b> Publikus: </b>
<ul>
 <li> Főoldal
 <li> Regisztráció
 <li> Bejelentkezés
</ul>


<b> Bejelentkezett: </b>
<ul>
 <li> Főoldal </li>
 <li> ToDo-k megtekintése </li>
 <ul>
 <li> Új ToDo felvétele </li>
 <li> ToDo módosítása </li>
 <li> ToDó megjelölése kész-ként </li>
 </ul>
</ul>

<h2>
Végpontok </h2>
<ul> 
 <li> GET/: főoldal </li>
 <li> GET/login: bejelentkező oldal </li>
 <li> POST/login: bejelentkező adatok felküldése </li>
 <li> GET/login/signup: regisztrációs oldal </li>
 <li> POST/login/signup: regisztrációs adatok felküldése </li>
 <li> GET/logout: kijelentkező oldal </li>
 <li> GET/todos/create: Új ToDo felvétele </li>
 <li> POST/todos/create: Új ToDo felvételehéz adatok felküldése </li>
 <li> GET/showmytodos: ToDo-k megjelenítése</li>
 <li> GET/:id/: ToDo megtekintése </li>
 <li> GET/:id/modify: ToDo módosítása </li>
 <li> POST/:id/modify: ToDo módosítása adatok felküldése </li>
 <li> GET/:id/markAsComplete: ToDo megjelölése kész-ként </li>


</ul>

