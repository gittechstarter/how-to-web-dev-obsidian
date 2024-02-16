CSS (Cascading Style-Sheets) ist für das Aussehen einer Website verantwortlich. Es arbeitet dafür mit Selektoren, denen anschließen eine Eigenschaft (Property) zugewiesen wird. Für eine ausführliche Erklärung schaut gerne hier: https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks
# Selektoren (Selectors)

Es gibt verschiedene Arten von CSS-Selektoren. Mit diesen können HTML-Elemente aus dem DOM ausgewählt werden, denen dann Eigenschaften (Properties) zugewiesen werden.

### Universal-Selektor
Dieser wählt alle Elemente auf einer Seite aus:
````
* {
	margin: 0px;
}
````

### Typ-Selektoren
Diese wählen ein HMTL-Element aufgrund seines Typs aus, z.B. alle `<h1>`-Elemente:

````
h1 {
	font-size: 20px;
}
````
### Attribut-Selektoren
Diese wählen HTML-Elemente aufgrund ihrer Attribute aus, z.b. alle mit dem Attribut `class`:

````
h1[class] {
	font-size: 20px;
}
h1[class="a"] {
	font-size: 20px;
}
````
wobei der erste Selektor alle `<h1>`-Elemente mit dem Attribut Klasse asuwählt, während der zweite alle `<h1>`-Elemente mit deren Klasse gleich "a" ist auswählt.

### Klassen-Selektoren
Diese wählen eine HTML-Elemente mit dem Attribut `class` aus:
````
<h1 class="a">HALLO</h1>
````
kann ausgewählt werden mit:
````
.a {
	font-size: 20px;
}
````

### ID-Selektoren
Diese wählen ein HMTL-Element anhand seines `id`-Attributes aus:
````
<h1 id="a">HALLO</h1>
````
kann ausgewählt werden mit:
````
#a {
	font-size: 20px;
}
````

## Pseudo-Klassen
Diese gehören auch zu den CSS-Selektoren, funktionieren aber ein wenig anders. Mit diesen Selektoren lassen sich Elemente auswählen, die sich in einem bestimmten Zustand befinden, z.B. ein Nutzer bewegt seinen Mauszeiger über das Element. Außerdem sind sie nützlich, wenn die Website selber HMTL-Elemente mit Hilfe von JS zum DOM hinzufügt. Es kann nämlich z.B. das erste Kind-Element eines HMTL-Elements ausgewählt werden. Dies ändert sich auch mit dem Einfügen neuer Elemente in den DOM nicht. Man nehme an wir haben folgende Struktur:
````
<div class="first">
	<p>Hallo</p>
</div>
````
Wir wollen nun das erste `<p>`-Element in dem Container mit der Klasse "first" immer fett gedruckt haben. Dann können wir dies mit folgendem CSS-Code erreichen:
````
.first p:first-child {
	font-weight: bold;
}
````
Mehr dazu in der [Referenz ](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements) 
## Pseudo-Elemente  
Pseudo-Elemente hingegen verhalten sich wie ein Wrapper um bestimmte Teile eines HTML-Element anzupassen. 

Soll z.B. die Größe der erste Zeile in allen `<p>`-Elementen angepasst werden, kann folgender CSS-Code genutzt werden:
````
p::first-line {    
	font-size: 30 px;
}
````

## Combinators (Kombinatoren)
CSS-Selektoren lassen sich auch kombinieren. Es gitb dafür verschiedene Möglichkeiten.

### Nachkommen-Kombinator (descendent combinator)
Dieser wählt alle Elemente aus die einen bestimmten "Vorfahren" haben, also innerhalb des DOMs in diesen verschachtelt sind:

````
body article p {
	font-size: 50 px;
}
````
Hier werden alle `<p>`-Elemente ausgewählt, die innerhalb des `<body>`-Element und dort innerhalb des `<article>`-Element verschachtelt sind.

### Kind-Kombinator (child combinator)
Dieser wählt alle Elemente aus, die direkte Kind-Elemente von einem Element sind.
Wir nehmen folgendes HTML an:
````
<div>
	<p> Das soll ausgewählt werden </p>
	<article>
		<p> Das soll NICHT ausgewählt werden </p>
	</article>
</div>
````
Hier wollen wir nur das erste `<p>`-Element auswählen. Das können wir mit folgendem CSS-Code erreichen:
````
div > p {
	font-size: 40px;
}
````
Es wird nur das `<p>`-Element ausgewählt, welches ein direktes Kind-Element von div ist. Wenn der Nachkommen-Kombinator genutzt worden wäre, wären alle `<p>`-Elemente ausgewählt worden.

### Next-sibling and subsequent-sibling combinator
Diese wählen, ausgehend von einem HTML-Element das nächste direkte Geschwister-Element bzw.  alle nächsten Geschwister-Elemente im DOM aus.

### Verschachtelte Selektoren
Erlauben sehr komplexe Kombinationen von Selektoren . Mehr dazu in der [MDN CSS Referenz](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators#creating_complex_selectors_with_nesting)

# Eigenschaften (Properties)

Sobald ein Element ausgewählt ist, können ihm Eigenschaften zugewiesen werden. Welche genutzt werden hängt vom Layout und dem HTML-Element ab. Schaut dafür gerne in die [Referenz](https://developer.mozilla.org/en-US/docs/Web/CSS).
# Cascade, specificity, inheritance

Tatsächlich gibt es einen Grund, warum CSS das Wort **cascading** im Namen hat. Dies soll ausdrücken, dass eine Reihenfolge bei der Anwendung von CSS-Eigenschaften gibt, die demselben HMTL-Element zugewiesen wurden. Dies kann der Fall sein, wenn wir Beispielweise einem Element direkt eine Eigenschaft zuweisen und danach, durch einen Selektor, dieselbe Eigenschaft mit einem anderen Wert definieren. Hier verändern wir ein `<h1 class="a">`-Element
````
h1 {
	font-size: 50px;
}

.a {
	font-size: 40px;
}
````
## Specifity
Nun wird bestimmt welcher der beiden Selektoren die höhere Spezifizität (specificty) hat. Dabei sind Klassen-Selektoren spezifischer als Typ-Selektoren. Daher hat das resultierende Element die Größe 40 Pixel. 

Allerdings haben Klassen- und Attribut-Selektoren sowie Pseudo-Klassen  die selbe Spezifizität. Was wird also angewendet? **In diesem Fall zählt immer die letzte Zuweisung in der CSS-Datei.**

## Inheritance (Vererbung)
Manche CSS-Eigenschaften werden von Eltern-Elementen im DOM an Kind-Elemente weitergegeben und andere nicht. Zum Beispiel vererbt dich die Farbgebung von Elementen an ihre Kind-Elemente. Dies kann geändert werden, indem diesen Kind-Elementen ihre eigene Farbe  zugewiesen wird (Spezifizität).
# Layout-Modelle



## Box-Modell

## Grid 

## Flexbox
# Media-Queries

Mit Media-Queries lassen sich CSS Befehle an verschiedene Ausgabegeräte anpassen.

# Animationen

CSS kann auch Animationen erzeugen. Dafür nutzt es Keyframes um die Positionen von HTML-Elementen auf einer Website zu unterschiedlichen Zeitpunkten zu definieren. Zwischen diesen Zeitpunkten wird dann "interpoliert". Die Interpolation bestimmt die Art und Weise mit der sich Objekte zwischen den Keyframes bewegen. 

````
.container {
    animation-duration: 20s; /*bestimmt die Dauer einer Animation in CSS*/
    animation-name: klein; 
}

  

/* Steuert Animation über Keyframes*/

@keyframes klein {

    from {

        margin-left: 100%;

        width: 300%;

      }

      to {

        margin-left: 0%;

        width: 100%;

      }

}
````


