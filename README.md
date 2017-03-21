# Invasion-der-Greeps
<h1 style="color:red;">Invasion der Greeps</h1>
<p>
<i>ein Projekt von Leif Peters und Linus Reck</i>
</p>
<p>Das vorliegende Programm wurde mit Hilfe "<mark>Greenfoot's</mark>" geschrieben. Beim Bearbeiten orientierten wir uns an unseren Vorkenntnissen aus den Stride-Angaben und dem Greenfoot-Buch, sowie nutzten wir nun verstärkt das Internet, so z.B. zur Inspieration.</p>
<p> Unser <a href="https://leynus.github.io/Stundenprotokoll/">Stundenprotokoll</a>
<h2>Inhaltsverzeichnis</h2>
<ul>
<li><a href="#anf">Anfänge</a></li>
<li><a href="#sdp">Sinn des Programms</a></li>
<li><a href="#ads">Ablauf des Spiels</a></li>
<li><a href="#adp">Ablauf der Programmierung</a></li>
<ul>
<li><a href="#era">Erste Actor</a></li>
<li><a href="#nah">Nahrungskette</a></li>
<li><a href="#zas">Zuschauer als Spieler</a></li>
<li><a href="#mus">Musik</a></li>
<li><a href="#for">Fortpflanzung</a></li>
<li><a href="#evh">Einführung von Hunger</a></li>
<li><a href="#sch">Die Schlange</a></li>
<li><a href="#zom">Zombiekrabben</a></li>
<li><a href="#gao">Game Over</a></li>
<li><a href="#sco">Der Score</a></li>
</ul>
<li><a href="#kla">Klassen</a></li>
<ul>
<li><a href="#cr1">crab.class</a></li>
<li><a href="#lob">lobster.class</a></li>
<li><a href="#sta">starfish.class</a></li>
<li><a href="#wor">worm.class</a></li>
<li><a href="#sna">snake.class</a></li>
<li><a href="#cr2">crab2.class</a></li>
<li><a href="#gam">gameover.class</a></li>
</ul>
<li><a href="#pfz">PLäne für die Zukunft</a></li>
</ul>
<h2 style="color:green;" id="anf">
Anfänge
</h2>
<p>Unsere eigentliche Idee war es, mit einem RaspberryPi zu arbeiten. In den ersten Stunden probierten wir dies aus und installierten ein neues Betriebssystem auf einem dieser Computer. Da wir uns diese Arbeit allerdings anders vorgestellt hatten, hörten wir recht schnell mit diesem Projekt auf und ließen uns eine neue Idee einfallen. Unser Ziel war (und ist) es ein Doppelkopfspiel mit Greenfoot zu programmieren. Dafür müssten wir uns aber erstmal mit dem Programm und Programmierung allgemein auseinandersetzen. Wir begannen mit den Greenfoot-Stride Lernaktivitäten. Später haben wir auf Grundlage dieser, eigene Ideen in die Welt gebracht, woraus nach einer Zeit ein Spiel entstanden ist. In unserem neuesten Projekt wanden wir uns den "Greeps"zu. Diese Aliens landen mit einem Raumschiff, um Tomaten zu sammeln.</p>
<h2 style="color:darkorchid;" id="sdp">
Sinn des Programms
</h2>
<p>Nach unserem ersten Projekt wendeten wir uns nun einer neuen Aufgabe zu. Diese besteht in der Optimierung der "Greeps". Durch später weiter erläuterte Regeln eingegrenzt, lassen sich die "Greeps" programmieren, so z.B. in welcher weise sie auf Wände reagieren.</p>
<h2 style="color:royalblue;" id="ads">
Ablauf des Spiels
</h2>
<p></p>
<img src="aufstellung.png" alt="aufstellung">
<h2 style="color:indianred;" id="adp">
Ablauf der Programmierung
</h2>
<h3 style="color:darkturquoise;" id="era">
Erste Actor
</h3>
<p>
</p>
<h3 style="color:darkturquoise;" id="nah">
</h3>
</p></p>
<h3 style="color:darkturquoise;" id="zas">
Zuschauer als Spieler
</h3>
<p>.</p>
<h3 style="color:darkturquoise;" id="mus">
Musik
</h3>
<p>.</p>
<h3 style="color:darkturquoise;" id="for">
Fortpflanzung
</h3>
<p></p>
<h3 style="color:darkturquoise;" id="evh">
Einführung von Hunger
</h3>
<p></p>
<h3 style="color:darkturquoise;" id="sch">
Die Schlange
</h3>
<p> </p>
<img src="snake.png" alt="snake">
<h3 style="color:darkturquoise;" id="zom">
Zombiekrabben
</h3>
<p></p>
<h3 style="color:darkturquoise;" id="gao">
Game Over
</h3>
<p>.</p>
<img src="game_over.png" alt="game_over">
<h3 style="color:darkturquoise;" id="sco">
Der Score
</h3>
<p>Um unser Programm mehr einem Spiel anzunähern, haben wir einen Score eingefügt. Dieser zählt die von der <a href="#wor">worm.class</a> entfernten Actor (Anzahl der Tiere, die der Wurm gefressen hat). Außerdem haben wir einen Zähler eingefügt, der mit jedem Durchlauf einen nach oben zählt.<br>
 Der Zähler „score“ zählt, die Durchläufe wie folgt:<br>
<mark>public static int score<br>
score = score + 1<br>
getWorld().showText („Your Score:“ + score, 100, 30)</mark><br>
Der Wert des Zählers wird an der Stelle (100 / 30) hinter „Your Score:“ gezeigt.
Wenn die <a href="#sna">snake.class</a> den Actor aus der World entfernt, hört der Zähler auf hochzuzählen.<br>
Der Zähler “eaten“ wird immer aktiviert, wenn eine if-Schleife durch das Berühren der <a href="#wor">worm.class</a> mit einem anderen Actor geöffnet wird. Sein Wert erscheint am Punkt (150 / 50) hinter „Number of eaten animals“.<br>
Er lautet wie folgt:<br>
<mark>public static int eaten<br>
if(isTouching(crab.class)) eaten = eaten + 1<br>
getWorld().showText („Number of eaten animals:“ + eaten, 150, 50)</mark><br>

Damit wir mit verschiedenen Klassen Zugriff auf die Variablen haben, sind diese auf public gesetzt. So konnten wir der <a href="#gam">gameover.class</a> der World den Befehl geben, mit diesen Werten zu arbeiten.
Um eine taktische Idee notwendig zu machen beim Spielen dieses Spiels haben wir diese beiden „Scores“ multipliziert zu einem Gesamtscore, der am Ende durch folgenden Code angezeigt wird:<br>
<mark>getWorld().showText („Final Score“ + Worm.eaten * Worm.score, 300, 250)</mark>
Anregungen zu dieser Einführung gab uns folgendes <a href="https://youtu.be/ubsC4PR2WjI">Video</a> von dem Erfinder Greenfoot's.</p>
<h2 id="kla" style="color:midnightblue;">Klassen</h2>
<h3 style="color:orchid;" id="cr1">crab.class<img src="crab.png" alt="crab"></h3>
<p><img src="crab_class_cut1.png" alt="crab_class">
Der Actor bewegt sich fünf Längeneinheiten pro Schleife vorwärts.<br>
Mit jeder Schleife zählt die Variable "TageSeitMahlzeit" einen hoch.<br>
Wenn das Objekt an den Rand der World trifft, dreht es sich mit einem zufälligen Winkel zwischen 45 und 90°.<br>
Trifft eine <a href="#cr1">crab.class</a> auf einen Actor der <a href="#sta">starfish.class</a>, wird der World befiehlt, einen neues Objekt der <a href="#cr1">crab.class</a> an einer zufälligen Stelle zu erzeugen. Außerdem wird dieser Actor der <a href="#sta">starfish.class</a> aus der World entfernt. Die Variable "TageSeitMahlzeit" wird zurück auf 0 gesetzt.<br>
Wenn die Variable "TageSeitMahlzeit" den Wert 300 erreicht, wird der World der Befehl gegeben, diesen Actor zu entfernen.
</p>
<h3  style="color:orchid;" id="lob">lobster.class<img src="lobster.png" alt="lobster"></h3>
<p><img src="lobster_class_cut1.png" alt="lobster_class"></p>
<p>Wenn der Actor auf eine <a href="#cr2">crab2.class</a> trifft, wird diese entfernt. Außerdem wird der World mitgeteilt dieses Objekt der <a href="#lob">lobster.class</a> zu entfernen.<br>
Der restliche Quelltext ähnelt dem der <a href="#cr1">crab.class</a> stark.
</p>
<h3 style="color:orchid;" id="sta">starfish.class<img src="starfish.png" alt="starfish"></h3>
<p><img src="starfish_class_cut1.png" alt="starfish_class"></p>
<p>Siehe <a href="#cr1">crab.class</a>, <a href="#lob">lobster.class</a>
</p>
<h3 style="color:orchid;" id="wor">worm.class<img src="worm.png" alt="worm"></h3>
<p><img src="worm1_class_cut1.png" alt="worm_class"></p>
<p>Wird die linke oder rechte Pfeiltaste gedrückt, dreht der Actor sich in die dementsprechende Richtung.<br>
Pro Schleife zählt die Variable "TageSeitMahlzeit" einen hoch.<br>
Wenn die Pfeiltaste nach oben bzw. nach unten gedrückt wird und der Wert der Variable "TageSeitMahlzeit" unter 300 liegt, bewegt sich das Objekt nach vorne bzw. nach hinten.<br></p>
<img src="worm2_class_cut1.png" alt="worm_class">
<p>Wenn der Actor ein Objekt der <a href="#sta">starfish.class</a>, <a href="#lob">lobster.class</a>, <a href="#cr2">crab2.class</a> wird die Variable "TageSeitMahlzeit" gleich Null gesetzt, das Objekt wird entfernt und die Variable "eaten" zählt einen nach oben. Wenn es sich um eine <a href="#cr1">crab.class</a> handelt, werden zusätzlich noch durch die Variablen "TodesortCrabX" und "TodesortCrabY" die aktuellen Koordinaten bestimmt und zu der Variable "Zombiecrab" wird 1 addiert.<br>
Der World wird befehligt, den Wert der Variable "eaten" hinter "Number of eaten animals" am Punkt (150 / 50)<br>
Ist die Variable "Zombiecrab" größer als Null, beginnt die Variable "ToteCrab" mit jeder Schleife +1 hochzuzählen.<br>
Ist diese bei 200 angelangt, gibt sie der World den Befehl einen neuen Actor der <a href="#cr2">crab2.class</a> auf den Punkt mit den durch "TodesortCrabX" und "TodesortCrabY" Koordinaten einzufügen. Die Variable "Zombiecrab" wird mit 1 subtrahiert und die Variable "ToteCrab" wird gleich Null gesetzt.<br>
Ist der Wert der Variable "tageSeitMahlzeit" bei 300 angelangt, wird der Y-Wert des Actors mit der Variable "Todesort" bestimmt. Dieser kann sich nur noch drehen. Der World wird befiehlt, einen Actor der <a href="#sna">snake.class</a> an den Punkt (0 / "Todesort").<br>
Die Variable "score" zählt mit jeder Schleife +1. Die World zeigt ihren Wert hinter "Your Score:" am Punkt (100 / 30).</p>
<h3 style="color:orchid;" id="sna">snake.class<img src="snake2.png" alt="snake2"></h3>
<p><img src="snake_class_cut1.png" alt="snake_class"></p>
<p>Der Actor bewegt sich in X-Richtung, entfernt bei Berührung den Actor der <a href="#wor">worm.class</a>, dreht sich um 180° bewegt sich vorwärts zurück an den Rand der World.<br>
Ist der Actor am Rand angelangt, wird der World befehligt, ein Objekt der <a href="#gam">gameover.class</a> am Punkt (300 / 200) einzufügen.</p>
<h3 style="color:orchid;" id="cr2">crab2.class<img src="crab2.png" alt="crab2"></h3>
<p><img src="crab2_class_cut1.png" alt="crab2_class"></p>
<p> Siehe <a href="#cr2">crab.class</a></p>
<h3 style="color:orchid;" id="gam">gameover.class<img src="gameover.png" alt="gameover_class"></h3>
<p><img src="gameover_class_cut1.png" alt="gameover_class"></p>
<p>Die Variablen "eaten" und "score" der <a href="#wor">worm.class</a> werden miteinander multipliziert und bei (300 / 250) als "Final Score:" angegeben.</p>
<h2 style="color:lime;" id="pfz">
Pläne für die Zukunft
</h2>
<p>Da uns die"Greeps" eine Herausforderung an unsere bisherigen Kenntnisse sind, ist es unser Ziel weiter an diesem Programm und in dieser optimierungsorientierten Weise zu arbeiten.</p>
