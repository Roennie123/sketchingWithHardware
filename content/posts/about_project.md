---
title: "Semesterprojekt"
date: 2023-07-26T13:09:01+02:00
featured_image: "/images/signal-2022-11-14-214744_022.jpeg"
draft: false
---

**Projektidee, Projektplan und Semesterverlauf**

Die Aufgabe dieses Semesters war es für „Sketching with Hardware“ ein eigenes Projekt zu konzipieren, planen, herstellen und zu präsentieren. Dieser Blogpost soll die Präsentation übernehmen.
Welches Projekt wir umsetzen blieb uns völlig frei. Es sollte nur folgende Kriterien (**Must-Haves**, Should-Haves) erfüllen:

•	**Kein stupides Nachbauen** bereits vorhandener Projekte\
•	Sinnvoller Einsatz von **Microcontroller**\
•	Mindestens ein **Fertigungsverfahren sinnvoll nutzen**\
•	**Interaktivität** in Form von Input/Output mit Nutzenden\
•	**Sicherheit**\
•	**Freigabe** durch Betreuer\
•	Bewegung bzw. Mechanik\
•	Vernetzung (z.B. mit App über Bluetooth oder WiFi, etc.)\
•	Sinnvolle Stromversorgung (Energiesparsamkeit)\
•	Finalprodukt (nicht mehr nur Prototyp)\

Da man sich bei zuviel kreativer Freiheit oft auch ein bisschen verliert (oder den Rahmen der Möglichkeiten aus den Augen verliert), habe ich mir meine eigenen Kriterien an das Projekt definiert:

•	Irgendwas in Richtung Robotik (Interesse & dazu null Erfahrung)\
•	Soll cool sein und optisch ansprechen\
•	Soll in gegebenem Zeitraum fertig werden (6 Wochen sind knapp)\
•	Möchte etwas Neues dazulernen

Habe dann alle Kriterien zusammengewürfelt und mich für eine Roboterschildkröte entschieden. Einfach weil ich damit alle Kriterien abdecken kann und mir die Idee gefallen hat mich 6 Wochen mit Schildkröten zu beschäftigen. Finde die nämlich ziemlich cool. 😊

Die Schildkröte sollte mit einer App steuerbar sein und laufen können (möglichst realistisch am eigentlichen Gang von Schildkröten orientiert). Außerdem wollte ich alles komplett selbst konstruieren/designen und das Gehäuse 3d-drucken. 

Nachdem meine Projektidee abgesegnet wurde, habe ich mich die ersten Wochen dann vor allem um die Planung und Prototypen zu den jeweiligen Funktionen gekümmert. 
Die Bewegung sollte von Motoren getragen werden. Am Anfang hatte ich die Überlegung mir hierzu eine Mechanik zu überlegen, um nur einen Motor für alles, oder einen pro Bein zu brauchen. Hatte dazu sogar mit dem Mechanikbaukasten ein Modell gebaut. Jedoch war die Bewegung garnicht so simpel und es hätte sehr, sehr viel Feinjustierung und Testdrucke benötigt um dieses Bewegungsmodell umzusetzen. Daher entschied ich mich dann für den sehr viel einfacheren Alternativplan, bei welchem pro Bein einfach zwei Motoren übereinander gestapelt werden welche dann summiert die nötige Bewegung ausführen können.
Um die Bewegung dann zu steuern, bzw.die Kriterien Vernetzung und  Interaktivität abzuhaken habe ich eine App generiert und ein Bluetoothmodul eingebaut. Hatte mir das komplizierter vorgestellt als es letztendlich war.

Für das 3D-Modell hatte ich mich entschieden zweigleisig zu fahren. Detaillierte, passgenaue Teile wie z.B. das Inlay für die Elektronik sollten mit Fusion (CAD-Tool) erstellt werden. Das eigentliche Schildkrötenmodell sollte aber etwas mehr Leben ausstrahlen als ein Montagebauteil. Daher sollte es in Blender modelliert werden.

Bisher hatte ich noch nie mit Blender gearbeitet, aber es stand schon immer auf meiner ToDo-Liste. Also habe ich mir die Zeit genommen das Programm so kennen zu lernen damit am Ende ein sehenswertes Projektergebnis herauskommt (Kriterium mit dem „möchte was neues lernen“ somit abgehakt). Wurde zwar gewarnt dass das Arbeiten mit Blender am Anfang oft etwas holprig sein kann, war dann aber doch überrascht wie aufwendig das war. Hab gefühlt zehnmal das Modell nochmal komplett überworfen und neu angefangen, da man immer wieder neue, bessere Methoden an ein Modell heranzugehen gelernt hat, je tiefer man eingetaucht ist. :D Man denkt es möglicherweise nicht, aber das war der schwerste Part des gesamten Projekts. Bin aber wahnsinnig froh über die Erfahrung und das den Umständen entsprechende Endergebnis, da das wie gesagt eh schon lange auf meiner ToDo-Liste stand.

Prinzipiell sollte die Schildkröte erstmal geradeaus laufen können. Was auch wunderbar funktioniert hat. Hatte mögliche Bewegungen darüber hinweg offen gelassen (je nach dem wie gut ich im Zeitplan stehe). Natürlich wäre es noch stark gewesen wenn sie sich ebenfalls drehen könnte bzw. lenkbar wäre. Dafür hat die Zeit dann aber nicht mehr gereicht.
Eine ursprüngliche Idee war es noch die Stromversorgung über ein Solarpanel (z.B. auf dem Bauch oder Panzer der Schildkröte) zu regeln. Denn Schildkröten gehören, wie alle Reptilien, zu den wechselwarmen Tieren. Diese können ihre Körpertemperatur z.B. durch Sonnenwärme hochfahren und aktiv werden. Was mit einer Stromversorgung über Sonnenlicht vergleichbar ist. Diese Idee habe ich dann aber verworfen, da selbst kleinere Solarpanele recht teuer sind und ich sonst relevantere Funktionen hätte streichen müssen um das Budget nicht zu überziehen.


**Tools und Methoden**

Mein Zeit- und Projektplan verlief zwar recht dynamisch, eine grobe Aufteilung der zu erledigenden Aufgaben kann aber folgendermaßen gemacht werden:

•	Gehäuse (3D-Model Schildkröte, 3D-Druck Schildkröte)\
•	Funktion (Mechanik, Verkabelung, Verlötung)\
•	Programmierung (Bewegungsabläufe, Kommunikation, App-Steuerung)

Anhand dieser Aufteilung möchte ich in diesem Abschnitt auf die von mir genutzten Methoden und Tools des Projekts eingehen. Wie gut ich mit einem Programm klargekommen bin habe ich folgendermaßen bewertet:  (sehr gut),  (passt),  (passt, brauche aber definitiv noch mehr Erfahrung),  (überhaupt nicht).
 
Als Fertigungsverfahren für das **Gehäuse** der Schildkröte schien mir der 3D-Druck am sinnigsten. Da man bis zu einem gewissen Grad man sehr detailliert werden kann und auch relativ groß. Außerdem sind Schildkrötenpanzer prädestiniert für FDM*-Drucker, da die Altersringe von Bauch und Panzer durch die Schichtung des Filaments besonders gut rauskommen.
Meinen Prototypen (um die Bewegungsabläufe schonmal grob zu definieren) habe ich mit dem Lasercutter aus einer dünnen Preßspanplatte geschnitten.

Genutzte Tools:\
•	**LightBurn**: Programm zur Erstellung des Schnittplans für den Lasercutter → Protoyp \
•	**Fusion**: Programm zur Erstellung von 3D-Volumenmodellen → passgenaue Bauteile für Servohalterung, Elektronikinlay, Motoraussparungen, komplettes Modell der Elektronik für Präsentation \
•	**Blender**: Programm zur Erstellung von 3D-Meshes bzw.späteren 3D-Modellen → alles organische wie Panzerober- und Panzerunterteil, Kopf, Schwanz und Beine \
•	**Cura**: Programm um STL-Dateien für den 3D-Druck mit einem Ultimaker zu slicen (Erstellung des G-Codes) → Druck von Schwanz, Panzerober- und Panzerunterteil, Kopf und Beinen \
•	**SnapmakerLuban**: Programm um STL-Dateien für den 3D-Druck mit einem Snapmaker zu slicen (Erstellung des G-Codes) → Druck von Servohalterung und Elektronikinlay \
•	**Microsoft 3D-Builder**: Programm um STL-Dateien für den 3D-Druck vorzubereiten → Vereinfachung und Reparatur von zu komplizierten oder kaputten Meshes um diese dann weiterzubearbeiten oder in Cura zu slicen \

Bei **Mechanik und Elektronik** habe ich mich für eine fast komplett reversible Methode entschieden, da ich mit 8 Motoren gearbeitet habe und mal mitbekommen habe dass diese auch durchbrennen können. Wollte also sichergehen dass alles verbaute auch irgendwie wieder austauschbar ist. 
Das habe ich durch eine Fixierung mit Schrauben oder Magneten umgesetzt bekommen. Lediglich die Beine wurden mit Zwei-Komponenten-Kleber an den Motorblättern fixiert. Hätte im Nachhinein auch dort besser mit Schrauben gearbeitet, da bereits zwei der Füße nachgeklebt werden mussten.
Außerdem sind die Motoren über gekürzte Jumperkabel mit der Platine und dem darauf verlöteten Microcontroller verbunden. Dadurch lassen sie sich sehr einfach wieder austauschen. Ebenso lässt sich die Stromversorgung jederzeit durch ein einfaches ausstecken unterbrechen.

Die **Programmierung** der Bewegungsabläufe war das mitunter einfachste des Projekts. Jedoch hatte ich etwas Schwierigkeiten damit, passende Loops zu bauen um eine direkte Unterbrechung der Bewegungsroutine zu initiieren (da die Schildkröte auf Kommando Laufen, sowie auch Stoppen soll).
An sich funktioniert das Prinzip hinter der Programmierung jedoch so, dass es Bewegungsmethoden gibt, welche mit einem speziellen Integer aufgerufen werden. User wählen eine gewünschte Bewegung für die Schildkröte in einer App aus, welche dann eine Zahl über Bluetooth an ein mit dem Microcontroller verbundenes Bluetoothmodul sendet. Diese Zahl wird vom Programm als Input entgegengenommen und in die zur Zahl passenden Bewegungsmethode umgesetzt. 
Genutzte Tools:
o	Arduino: Programm zum Schreiben, Kompilieren und Hochladen von Code für den Microcontroller in C → Programmcode für Bewegung. Es gab ein paar Probleme mit Updates und Versionsnummern für die entsprechenden Boards 
o	MIT App Inventor: Programm um Apps zu designen, zu erstellen und den Interfacekomponenten dann einen Code zuzuweisen → Erstellung der App „walking tortoise“ 


**Motivation**

Am meisten motiviert hat mich, dass ich mir eigentlich relativ sicher war dass mein Projekt in dem gegebenen Zeitraum auch zu schaffen ist. Zwar musste man sich dafür auch gut dahinterklemmen, und hatte ein paar Mal auch ein  bisschen Zweifel (z.B. ob die Motoren das finale Schildkrötengewicht überhaupt packen), aber diese konnten sich zum Glück beseitigen. Die Ungewissheit darüber dass es vllt.doch nicht fertig wird, hätte mich wahnsinnig demotiviert.

Auch wenn ich die Themenwelt Robotik nur ganz leicht gestriffen habe, weis ich nun trotzdem ein bisschen mehr über den Umgang mit Motoren.
Was jedoch am meisten Früchte tragen wird für meine persönliche Zukunft ist, dass ich endlich mal Blender kennengelernt habe, und hoffe dass ich damit auch in Zukunft noch weiterarbeiten werde. Aber selbst wenn nicht besteht jetzt der Bezug dazu.

Ob der Kurs inhaltlich einen Einfluss auf meine berufliche Zukunft hat kann ich leider nicht sagen. Könnte mir nichts cooleres vorstellen, als irgendwie im „Prototypenbau“ mitzuwirken und eine schöne Mischung zwischen konzipieren und bauen (damit ist auch die Umsetzung von irgendwelchen Modellen zu Hardware gemeint) in möglichst kleinen Teams zu haben. Könnte mir aber vorstellen dass diese Traumjobs finanzielle eher unsicher gestaltet werden.

Jedoch lassen sich die Erfahrungen welche ich in Projektplanung und -umsetzung gemacht habe direkt auf zukünftige Herausforderungen im beruflichen Kotext übertragen. Bisher habe ich oftmals in Teams gearbeitet (was bei diversen Tätigkeiten auch unumgänglich ist), muss aber zugeben, dass mir diese eigenverantwortliche Soloplanung auch sehr gut gefallen hat. Alles hat seine Vor- und Nachteile. :D

Was in einem Team z.B. selten passiert, ist das Abdriften in unnötige Kleinigkeiten. Hatte mir z.B. eine bestimmte Schildkrötenart ausgesucht und 3 Tage damit verbracht dass das Modell dann auch als diese Art erkennbar ist, bis mir klar wurde, dass es am Ende niemanden juckt welche Art das ist. Nicht mal mich selbst. Mit einem Team im Rücken wäre schon längst jemand vorbeigekommen und hätte diesen Irrweg beendet.


**Zukunftswünsche für den Kurs**

Mir hat der Ablauf und die Führung des Kurses sehr gefallen. Die Anforderungen waren so gesetzt, dass man zwar viel Freiheit, aber auch einen angenehmen eingrenzenden Rahmen hatte. Außerdem durften wir sehr selbstständig Arbeiten ohne kontrollierende Blicke über die Schulter. Bei Fragen stand aber immer ein Betreuer mit Rat und Tat zur Seite und es wurden sogar Überstunden gemacht um Probleme zu lösen. Wir wurden also nie allein gelassen wenn wir das nicht auch wollten. Bin ein riesen Fan dieser Arbeits- und Lernweise und wünsche mir für zukünftige Jahrgänge dass sie ebenfalls diese Erfahrung machen dürfen.

Da wir in diesem Abschnitt Wünsche äußern dürfen: SLA-Druck kann definitiv ebenfalls zu den aktuellen Fertigungsverfahren dazugezählt werden. Hätte ich diesen sehr gerne ausprobiert. Mir ist allerdings bekannt dass die Abzugsanlage noch nicht darauf vorbereitet ist. Vielleicht lässt sich das ja einrichten für die zukünftigen Jahrgänge (also eine Abzugsanlage oder ein extra Raum so dass der Drucker den Gesundheitsrichtlininien entspricht und freigegeben werden kann).
