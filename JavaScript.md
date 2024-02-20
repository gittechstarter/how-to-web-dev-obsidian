JS besitzt alle grundlegenden [Programmierkonzepte]. Darüber hinaus besitzt JS noch spezifische Funktionalitäten, die besonders wichtig für Webdevelopment sind. Diese werden im folgenden besprochen

# JavaScript-Objekte

Objekte existieren in vielen Programmiersprachen. Sie sind ein nutzer-definierter Datentyp und wurden im Zuge der [Objekt-orientierten Programmierung](https://de.wikipedia.org/wiki/Objektorientierte_Programmierung) erstmalig eingeführt. I.d.R. besitzen Objekte Funktionen und Variablen, die angesprochen werden können, sobald man ein Objekt initialisiert hat.

````
const person = {
  name: ["Bob", "Smith"],
  age: 32,
  bio: function () {
    console.log(`${this.name[0]} ${this.name[1]} is ${this.age} years old.`);
  },
  introduceSelf: function () {
    console.log(`Hi! I'm ${this.name[0]}.`);
  },
};

````

Hier sieht man eine solches Objekt. Es sieht sehr ähnlicher einer JSON-Datei aus. Warum? JSON steht für JavaScript Object Notation und wird genutzt um strukturierte Daten (Key-Value Paare) zu speichern.  Es ist dafür stark an der JS-Objekt-Syntax angelehnt. 

Das obige Objekt besitzt die Variablen `name`, `age` und die Funktion `bio` und `introduceSelf`. Variablen können mit folgender Syntax abgerufen werden:
````
person.age
````
Funktionen können hingegen mit folgender Syntax abgerufen werden:
````
person.bio()
````

# DOM-Interaktion

Ein wichtiges Objekt in JS ist das `document`-Objekt. Mit dessen Hilfe kann mit dem DOM interagiert werden. Dabei können wir die "eingebauten" Variablen und Funktionen des `document`-Objekts nutzen. Z.B. lässt sich ein Element anhand seiner ID auswählen:

````
h1 = document.getElementByID("header");
````

Dessen Eigenschaften (Properties) können dann ebenfalls mit JS manipuliert werden:

````
h1.style.font-size = "12px";
````

Außerdem können HMTL-Elemente mit Hilfe von JS erstellt werden:

````
h1 = document.createElement("h1")
`````

Dieses muss dann in den DOM-Baum integriert werden:

````
document.body.appendChild(h1)
````

Mehr dazu in der [MDN-Referenz](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents).
# Events

Events werden durch die Interaktion eines Nutzers mit einer Webseite produziert. Es kann sich z.B. um Klicks auf oder auch Hovering über ein HTML-Element handeln.


Mehr dazu in der [MDN-Referenz.](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)



# Web-APIs
# Asynchrone Programmierung



