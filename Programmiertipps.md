Am Anfang einer Karriere in IT kann die Komplexität aller Konzepte, die es zu erlernen gilt, überwältigend sein. Dabei kann man schnell aus den Augen verlieren, dass es am Ende nur auf einige grundlegende Dinge ankommt.

# Das IT-Mindset

Was ist ein guter ITler? Eine Person, die besonders viele Programmiersprachen kennt? Eine Person, die besonders gut Linux bedienen kann? Eine Person, die besonders viele Zertifikate hat? Natürlich macht dies alles keinen guten Programmierer aus. Alles was ich oben genannt habe sind nämlich nur Werkzeuge um ein Problem zu lösen. Das kann, z.B., das Aufsetzen einer Serverumgebung in Linux oder das Erstellen einer Web-App für ein Unternehmen sein. Alle größeren Aufgaben in der IT zeichnen sich vor allem durch ihre Komplexität aus. Der wichtigste Skill den ein ITler daher haben kann ist Problemlösefähigkeiten. Oder anders gesagt: Wie Unterteile ich mein komplexes Projekt in kleinere Einheiten, von denen ich weiß, wie ich sie lösen kann? Dies überträgt sich auch auch auf das Programmieren. Nur wer ein komplexes Programm in einzelne Funktionen zerlegen kann bzw. versteht welche Funktionen es braucht um dieses Programm zu schreiben, kann auf Dauer erfolgreich in der IT sein. Es ist daher essentiell die eigene Problemlösekompetenz zu stärken und ständig daran zu arbeiten. 

Ein wichtiger Schritt für die Problemlösung ist die Problemdefinition. Die wird meist durch [Modellierung](https://de.wikipedia.org/wiki/Softwaredesign) erreicht. Dafür nutzt man in der IT Modellierungssprachen wie [UML](https://de.wikipedia.org/wiki/Unified_Modeling_Language) oder auch [FMC](https://de.wikipedia.org/wiki/Fundamental_Modeling_Concepts). Dabei werden Methoden wie z.B. [Objektanalyse](https://de.wikipedia.org/wiki/Objektorientierte_Analyse_und_Design) eingesetzt.

Allerdings bedeutet es nicht, dass man bei jedem Problem diese teilweise umständlichen Methodiken anwenden muss. Meist reicht es, sich mit Stift und Papier eine Zeichnung zu erstellen und ein wenig zu Brainstormen. Da dies aber eine sehr individuelle Sache ist, muss jeder für sich selber herausfinden, was die beste Arbeitsweise ist.

# Chat-GPT

Mir ist bewusst, dass man mit Chat-GPT schnell vorankommt. Ich glaube auch das es sicherlich seine Berechtigung als Hilfsmittel im IT-Bereich hat. Aber gerade für Anfänger kann dies schnell zum Problem werden. Natürlich kann ich mir von Chat-GPT schnell eine Website zusammenbauen lassen. Allerdings hilft mir dies wenig, sobald ich diesen Code anpassen möchte. Ich muss verstehen, was der Code tut oder zumindest verstehen, was ich Chat-GPT fragen muss um den Code verstehen zu können. Die Qualität von Generative AI ist nach wie vor stark von der Qualität der Fragen (Prompts) abhängig. Weiß ich also nicht was ich zu fragen habe, kann ich mir auch mit Chat-GPT nur begrenzt helfen. Gerade für Anfänger ist Chat-GPT daher mit Vorsicht zu nutzen. Ich folgendes Vorschlagen: Nutzt Chat-GPT als eine Art Google und nicht dafür euch eine komplette Code-Base generieren zu lassen. Wenn ihr in der Modellierung, bzw. der Unterteilung eines Problems in Untereinheiten korrekt vorgegangen seid, könnt ihr Chat-GPT zur Lösung dieser kleinen Probleme nutzen. Dies hat den Vorteil, dass ihr viel bessere Ergebnisse bekommt, da euere Fragen zielgerichteter sind. 

Darüber hinaus sollte man sich bei Chat-GPT immer über Folgendes im Klaren sein:
1. Hallucinations
Chat-GPT kann manchmal "Dinge erfinden". Diese nennen sich Hallucinations, weil die AI im Prinzip Dinge halluziniert, die nicht existieren.
2. Datenschutz
Open AI trainiert ihr  Modell mit Hilfe von "Reinforcement Learning with Human Feedback". D.h. , dass eure Prompts von Menschen gereviewt werden und es daher potenziell Probleme beim Datenschutz gibt. Daher hat Chat-GPT am Arbeitsplatz nichts zu suchen und dies sieht euer zukünftiger Arbeitgeber wahrscheinlich genauso.
 3. Datenbasis
Alle AI-Modelle sind nur so gut, wie die Daten auf denen sie trainiert wurden. Daher kann es sein, dass Chat-GPT euch Vorschläge aufgrund von veralteten Daten macht. Gerade in der IT, wo alles sehr schnelllebig ist, kann es daher sein, dass Code der von Chat-GPT generiert wird nicht den neusten Standards entspricht 
# Code verstehen: Referenzen und Dokumentationen

Sicherlich habt ihr schon vor dem Problem gestanden: Ihr habt einen Code und wisst nicht was er tut. In diesem Falle kann man Chat-GPT fragen. Es lohnt sich aber oft auch eine Blick in Referenzen und Dokumentationen zu werfen. I.d.R. geben Dokumentationen einen Überblick über die Struktur und Nutzung des Codes, während Referenzen die Nutzung einzelner Bestandteile dokumentieren. Für uns als Webdevs sind die wichtigsten Referenzen und Dokumentationen die [Mozilla Developer Docs](https://developer.mozilla.org/en-US/) und [W3schools](https://www.w3schools.com/).

Aber wie lese ich Referenzen? Man nehme an ich möchte die fetch-Funktion von JavaScript nutzen. Dann kann in den Mozilla Dev Docs schauen und findet folgenden Eintrag:

![[Pasted image 20240213140013.png]]Hier sieht man exemplarisch wie Referenzen funktionieren. Wir haben eine kurze Beschreibung der Funktion und können verstehen ob sie für unseren Use-Case wertvoll ist. Danach folgen meist Parameter der Funkion:
![[Pasted image 20240213140246.png]]
Hier können wir sehen, was wir an eine Funktion übergeben können und was die einzelnen Parameter bewirken. Zusätzlich sehen wir welche Parameter nötig und welche optional sind.
Dann gibt es meist noch Informationen über Rückgabe-Werte und mögliche Fehler:
![[Pasted image 20240213140457.png]]Zusätzlich gibt es für die fetch-API noch eine komplette [Dokumentation](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API), die uns die Verwendung erklärt. Mit diesen Materialien sind wir dann im Stande die fetch-API in unserem Code zu nutzen