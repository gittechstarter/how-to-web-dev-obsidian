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
Wir sehen dass HTML aus verschiedenen Elementen besteht, die mit spitzen Klammern ausgezeichnet werden. Dabei gibt es immer ein öffnendes Element und ein schließendes. Die beiden unterscheiden sich durch ein Slash-Symbol, z.B. öffnend: `<title>` und schließend `</title>`. Weitherhin sehen wir das sich Elemente verschachteln lassen. So steht das `<h1>`-Element und das `<p>`-Element innerhalb des `<body>`-Elements.Außerdem sehen wir das es ein `<head>`-Element und ein `<body>`-Element gibt. Wir haben gelernt, dass HTML Metadaten speichern kann. Diese kommen innerhalb des `<head>`-Element unter. Metadaten sind Daten über Daten, z.B. 