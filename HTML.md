>**Hypertext Markup Language** (**HTML**, [englisch](https://de.wikipedia.org/wiki/Englische_Sprache "Englische Sprache") für _[Hypertext](https://de.wikipedia.org/wiki/Hypertext "Hypertext")-Auszeichnungssprache_) ist eine textbasierte [Auszeichnungssprache](https://de.wikipedia.org/wiki/Auszeichnungssprache "Auszeichnungssprache") zur Strukturierung [elektronischer Dokumente](https://de.wikipedia.org/wiki/Elektronisches_Dokument "Elektronisches Dokument") . [HTML-Dokumente](https://de.wikipedia.org/wiki/Webseite "Webseite") sind die Grundlage des [World Wide Web](https://de.wikipedia.org/wiki/World_Wide_Web "World Wide Web") und werden von [Webbrowsern](https://de.wikipedia.org/wiki/Webbrowser "Webbrowser") dargestellt. Neben den vom Browser angezeigten Inhalten können HTML-Dateien zusätzliche Angaben in Form von [Metainformationen](https://de.wikipedia.org/wiki/Metadaten "Metadaten") enthalten.
>Quelle: https://de.wikipedia.org/wiki/Hypertext_Markup_Language

Wie man hier schön entnehmen kann ist HTML eine Sprache zur Strukturierung von Dokumenten die dann als Website dargestellt werden kann. Ein Webbrowser interpretiert also HTML-Dateien um eine Website anzuzeigen. Außerdem können wir Metainformation in HMTL unterbringen. Dafür schauen wir uns erstmal folgendes Snippet an:
````
<!DOCTYPE html>  
<html>  
<head>  
	<title>Page Title</title>  
</head>  
<body>  
  
	<h1>This is a Heading</h1>  
	<p>This is a paragraph.</p>  
  
</body>  
</html>
````
Wir sehen dass HTML aus verschiedenen Elementen besteht, die mit spitzen Klamern ausgezeichnet werden. Dabei gibt es immer ein öffnendes Element und ein schließendes. Die beiden unterscheiden sich durch ein Slash-Symbol, z.B. öffnend: `<title>` und schließend `</title>`. Weitherhin sehen wir das sich Elemente verschachteln lassen. So steht das `<h1>`-Element und das `<p>`-Element innerhalb des `<body>`-Elements.Außerdem sehen wir das es ein `<head>`-Element und ein `<body>`-Element gibt. Wir haben gelernt, dass HTML Metadaten speichern kann. Diese kommen innerhalb des `<head>`-Element unter. Metadaten sind Daten über Daten, z.B. der Titel der Website welcher im `<title>` -Element festgelegt wird.

# Attribute

HTML-Elemente besitzen Attribute. Attribute bieten die Möglichkeit Informationen in HTML-Elemente einzubetten. Schaut euch dafür gerne folgende Seite an: https://www.w3schools.com/html/html_attributes.asp .  Es wird dabei in **globale** Attribute und Attribute, die **spezifisch** für bestimmte Elemente sind. Außerdem ermöglichen es Attribute CSS oder auch JS in HTML zu integrieren

# Gruppieren von Elementen

Oft hat man in HTML das Problem, dass man Elemente gruppieren möchte, um sie gemeinsam mit Hilfe von CSS oder JS zu verändern. Dafür spielt das `<div>`-Element eine besondere Rolle. Es dient als eine Art Container für andere Elemente und hat ansonsten keine direkte Funktion. Meist wird dem `<div>`-Element dabei ein Klassen- oder ID-Attribut gegeben, um es später mit Hilfe von CSS-Selektoren ansprechen zu können. Die Gruppierung an sich wird durch Verschachtelung erreicht:

````
<!DOCTYPE html>  
<html>  
<head>  
	<title>Page Title</title>  
	<link rel="stylesheet" href="styles.css"></link>
	<script src="script.js"></script>
</head>  
<body>  
	  <div class="container">
		<h1>This is a Heading</h1>  
		<p>This is a paragraph.</p>  
	  </div>
</body>  
</html>
````
Dieser Code gruppiert das `<h1>`-Element mit dem `<p>`-Element innerhalb des `<div>`-Elements mit der Klasse "container".
# Integration von CSS und JS

CSS und JS werden in HTML i.d.R in den Metadaten (also innerhalb des  `<head>`-Element) hinterlegt. Warum müssen wir diese Dateien in der HTML refernzieren? Das liegt daran, dass der Browser immer zuerst eine .html Datei interpretiert und wenn er dabei auf die Referenzen zur CSS und JS Datei stößt fängt er an diese auszuwerten. Sind sie allerdings nicht referenziert, kann der Browser die Dateien "nicht sehen". Um zu verstehen wie das praktisch funktioniert, schauen wir uns folgendes Snippet an:

```
<!DOCTYPE html>  
<html>  
<head>  
	<title>Page Title</title>  
	<link rel="stylesheet" href="styles.css"></link>
	<script src="script.js"></script>
</head>  
<body>  
  
	<h1>This is a Heading</h1>  
	<p>This is a paragraph.</p>  
  
</body>  
</html>
````
Hier sehen wir nun ein `<script>`-Element und ein `<link>`-Element.  Das `<script>`-Element  integriert JavaScript in unsere HTML-Datei. Es nutzt dafür das `src`-Attribute des Elements, indem es den Namen der JS-Datei "script.js" nutzt. Hier wird jedoch ein Pfad angegeben. Nutzen wir nur den Namen, muss sich diese Datei also im selben Ordner wie die .html Datei befinden.

CSS wird hingegen mit dem `<link>`-Element eingebunden. Es nutzt dafür das `rel`-Attribute und das `href`-Attribute. Hier wird die Datei mit dem Namen "style.css" verlinkt. Hier steht wieder ein Pfad dahinter, die Datei muss sich also im selben Pfad wie die .html-Datei befinden. Die Namen der Dateien an sich sind gleichgültig. Es gibt jedoch die Konvention sie jeweils so zu bennen.

# Document Object Model (DOM)

>Das DOM ist ein API, um HTML-Elemente aus einem HTML-Dokument auszuwählen und zu verändern.
>Quelle: [MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Using_the_Document_Object_Model#what_is_a_dom_tree)

Diese Definition mag erst einmal verwirrend klingen. Aber im Grunde ist es ganz einfach. Um Dinge mit CSS oder auch JS in HTML zu verändern, brauchen wir eine Möglichkeit wie wir auf diese Dinge zugreifen können. Es braucht ein Modell, womit wir einzelne Elemente innerhalb einer HTML-Datei verorten können. Diese Lücke wird durch das DOM geschlossen. 

Das DOM basiert auf einer Baumstruktur mit. Der Baum beginnt mit dem `Document`-Element. Dieses nennt man auch Wurzel-Element. Davon gehen dann das `Head`- und das `Body`-Element ab. Dabei wird das `Document`-Element als Eltern-Element (Parent) gegenüber dem `Head`- und `Body`-Element bezeichnet. Diese sind jeweils die Kind-Elemente (Children) des `Document`-Elements. Die Elemente `Head` und `Body` werden wiederum als Geschwister (Siblings) bezeichnet.

![[DOM_grafik.jpg]]






