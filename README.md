1.3.4:

In Kürze: Inhalte müssen sowohl in Hoch- wie auch Querformat angezeigt und bedient werden können. Dies ermöglicht selber zu entscheiden, ob Inhalte im Hoch- oder im Querformat bevorzugt werden.

Menschen mit bestimmten Behinderungen arbeiten mit einem fix montierten Ausgabegerät, z.B. mit einem an einem Rollstuhl befestigten Smartphone (physisch in einer Halterung verankert). Ihnen ist es nicht möglich, das Gerät zu drehen. Menschen mit starker Sehbehinderung bevorzugen unter Umständen die Quer-Orientierung des Smartphones, weil Inhalte dann potenziell grösser dargestellt werden. Es ist deshalb wichtig, dass Web-Inhalte (Anmerkung: finde das Wort "Web-Inhalte" gut! Könnten wir noch versuchen zu extrapolieren auf meine EKs) sowohl im Hoch- als auch im Querformat angezeigt und bedient werden können. Siehe auch 1.4.10.

Passt sich der Inhalt nicht automatisch an die Bildschirmorientierung an, muss ein Schalter angeboten werden zum manuellen Drehen des Bildschirminhalts.

Hinweis: Ausnahmen sind Anwendungsfälle, bei denen eine spezifische Bildschirmorientierung vorausgesetzt wird, etwa eine Klavier-App, welche das Querformat benötigt, um genügend Tasten darzustellen (bzw. wo die benötigte Anzahl Tasten im Hochformat zu eng dargestellt werden müsste).

Verantwortlichkeiten:
- Das Designteam definiert Ansichten, die sowohl im Hoch- wie auch im Querformat angezeigt und genutzt werden können.
- Das Entwicklungsteam setzt die vom Designteam erarbeiteten Voraben sorgfältig um und sorgt in der Programmierung dafür, dass alle Inhalte in beiden Bildschirmausrichtungen korrekt angezeigt werden und bedienbar sind.

1.3.5:

In Kürze: Bei Formularen mit Angaben zur eigenen Person muss der Eingabezweck der entsprechenden Formularfelder maschinenlesbar sein (autocomplete-Attribut). Dies ermöglicht das automatische Ausfüllen derselben, was insbesondere Menschen mit kognitiven und motorischen Einschränkungen zugute kommt.

Alle Menschen, insbesondere aber diejenigen mit kognitiven Behinderungen, profitieren von klar beschrifteten Eingabefeldern. Menschen mit motorischen Behinderungen profitieren vom automatischen Ausfüllen von Formularfeldern, weil dadurch die Notwendigkeit feinmotorischer Bewegungen reduziert wird. Programmatische Methoden können diesen Menschen helfen, den Zweck eines Eingabefeldes zu erkennen und Antworten voreinzugeben. 

Damit Benutzeragenten Formularfelder automatisch ausfüllen können, wird der korrekte Einsatz des autocomplete-Attributs vorausgesetzt. So wird sichergestellt, dass programmiertechnisch diejenigen Felder vorbefüllt werden können, zu denen die Daten bereits vorliegen. 

Wichtig: Dies trifft nur auf Formularfelder zu, die Daten über die Person sammeln. Eine abschliessende Liste der möglichen 53 Werte findet sich unter https://www.w3.org/TR/WCAG21/#input-purposes

Hinweis: Sowohl fehlende als auch falsche autocomplete-Attribute (etwa autocomplete="birthday" statt autocomplete="bday") verletzen dieses Erfolgskriterium.

Verantwortlichkeiten:
- Das Entwicklungsteam versieht jedes Formularfeld, das Daten über die ausfüllende Person sammelt und in der Liste unter https://www.w3.org/TR/WCAG21/#input-purposes aufgeführt ist, mit dem passenden autocomplete-Attribut.

1.4.10:

In Kürze: Inhalt muss sich den Viewport-Mindestdimensionen anpassen (sog. Reflow). Dies ermöglicht sehbehinderten Menschen, alle Inhalte auch bei hoher Vergrösserung nutzen zu können, ohne in mehr als eine Richtung scrollen zu müssen.

Sehbehinderte Menschen arbeiten häufig mit niedriger Bildschirmauflösung und/oder hohem Zoom-Faktor. Web-Inhalte müssen entsprechend auch unter diesen Umständen korrekt angezeigt werden (ohne Überlappungen oder sonstwie störende Effekte), wobei nur in eine Richtung gescrollt werden darf (entweder horizontal oder vertikal, nicht aber beides). Siehe auch 1.3.4.

Die vorgegebene Mindest-Auflösung hierfür ist 320x256 CSS-Pixel.

Ausnahmen: Bei Bildern, Karten, Diagrammen, Videos, Spielen, Datentabellen und Webapplikationen, bei denen eine Toolbar sichtbar bleiben muss, darf auch in zwei Richtungen gescrollt werden.

Verantwortlichkeiten:
- Das Designteam definiert die Inhalte so, dass der Reflow berücksichtigt wird.
- Das Entwicklungsteam setzt die vom Designteam definierten Vorgaben sorgfältig um. Es sorgt dafür, dass der Reflow funktioniert wie vorgeschrieben. 
- Die Inhaltsverantwortlichen kontrollieren die erstellten Inhalte auf ihre korrekte Darstellung in den Viewport-Mindestdimensionen. Sind etwa Wörter zu lang und führen zu einem Scrollbedarf in mehrere Richtungen, sind die Inhalte entsprechend anzupassen.

1.4.11:

(Anmerkung: Habe hier an 1.4.2 angeglichen. Ist vielleicht jetzt zu stark vereinheitlicht und muss es auch nicht unbedingt sein.)

In Kürze: Bedienelemente (z.B. Textfelder, Radiobuttons, Checkboxen, Schalter, Tabs) und grafische Elemente (z.B. Linien eines Diagramms) müssen sich farblich durch genügend Kontrast vom Hintergrund abheben. Dies ermöglicht es Menschen mit Sehbeeinträchtigung, dieselben erkennen und lesen zu können.

Menschen mit Sehschwäche und Fehlsichtigkeit sind darauf angewiesen, dass sich Elemente gut sichtbar vom Hintergrund abheben. Deshalb müssen Bedienelemente und grafische Elemente einen ausreichend hohen Kontrastwert zum Hintergrund aufweisen.

Jeder visuelle Hinweis, der für die Wahrnehmung und Bedienung erforderlich ist, insbesondere auch um den Zustand eines Elements zu interpretieren, muss einen Kontrastwert von mindestens 3:1 aufweisen (Anmerkung: würde den Wert nicht in Klammern setzen, der ist wichtig!). Das gilt z.B. für Formularfeldbegrenzungen, Ausklappindikatoren bei Dropdowns, das Häkchen einer Checkbox, etc. Wenn zudem die Farbe eines Bedienelements ändert (etwa bei Fokus oder Aktivierung), dann muss auch diese Farbe die Kontrastmindestanforderung erfüllen. An den Hover-Zustand hingegen werden keine Anforderungen gestellt.

Bei Schaltern wird empfohlen, den klickbaren Bereich ebenfalls ausreichend kontraststark zu umranden. Solange allerdings aufgrund von Position, Schriftart, etc., ein Schalter klar als solcher wahrnehmbar ist, ist eine kontraststarke Beschriftung ausreichend. Bei Textfeldern mit kontraststarkem Platzhaltertext bestehen keine Kontrastanforderungen an die Feldbegrenzungslinien. Siehe diesbezüglich auch 1.4.3.

Ausreichende Kontraste in und von grafischen Elementen bedeuten, dass jeder visuelle Hinweis, der für die Wahrnehmung und die Bedienung erforderlich ist, einen Kontrastwert von mindestens 3:1 aufweisen muss. Gemeint sind damit z.B. Kurven und Linien eines Diagramms, darin enthaltene Symbole, Beschriftungen, etc. 

Hinweis: Rein dekorative Grafiken sind nicht gemeint. Die Anforderungen an den Mindestkontrast gelten nur für sinntragende, informative grafische Elemente. (Anmerkung: Steht eigentlich unter 1.4.3 schon so, aber vielleicht ist Redundanz hier angebracht?)

Tipp: Zerlegen Sie komplexe Grafiken in ihre kleinsten aussagekräftigen Teile. Prüfen Sie für jedes Teil dessen Kontrast zu den angrenzenden Farben.

Verantwortlichkeiten:
- Das Designteam definiert eine Palette von Vorder- und Hintergrundfarben, die in den benötigten Kombinationen genügend Kontrast aufweisen.
- Das Entwicklungsteam setzt die vom Designteam definierten Vorgaben sorgfältig um.
- Die Inhaltsverantwortlichen gestalten Inhalte so, dass diese genügend Kontrast aufweisen.
- Projektverantwortliche sollten sich bewusst sein, dass kontraststarke Designs (auch über die Mindestanforderungen hinaus) ein Vorteil für alle Sehenden sind.

1.4.12:

In Kürze: Menschen mit Sehbehinderungen können für sich die Lesbarkeit von Texten verbessern, indem sie Werkzeuge wie Bookmarklets oder eigene Stylesheets nutzen. So können sie die Abstände zwischen Zeilen, Absätzen, Worten und Zeichen anpassen. Dass kann dazu führen, dass die Texte mehr Platz benötigen. Solche Abstandsanpassungen müssen möglich sein, ohne dass Inhalt oder Funktionalität verloren gehen. 

Hinweise: 
- Das gilt nur, wenn die Seite echten Text enthält (also Text, der nicht über eine Grafik bereitgestellt wird). Für Anforderungen in Bezug auf Bilder eines Textes, beachten Sie Erfolgskriterium 1.4.5.
- Die Anforderung verlangt nicht, dass das Entwicklungsteam die genannten Werte in der Programmierung umzusetzen, sondern lediglich, dass im Browser vorgenommene Anpassungen nicht zum Abschneiden bzw. Überlappen von Text oder Verlust von Funktionalitäten führt.

Bei Textinhalten müssen die Abstände von Zeilen, Absätzen, Wörtern und Buchstaben auf die folgenden Werte anpassbar sein oder diese Werte bereits aufweisen, ohne dass Funktionalitäten oder Inhalte verloren gehen oder Darstellungsprobleme (z.B. Überlappungen von Text, abgeschnittener Text, nicht mehr angezeigter Text) entstehen (und ohne die gleichzeitige Anpassung anderer Eigenschaften):
- Linienhöhe (line-spacing) zu mindestens dem 1.5-fachen der Schriftgrösse (font-size);
- Abstand nach Absätzen zu mindestens dem 2-fachen der Schriftgrösse;
- Wortabstand (word-spacing) zu mindestens dem 0.16-fachen der Schriftgrösse;
- Zeichenabstand (letter-spacing) zu mindestens dem 0.12-fachen der Schriftgrösse.

Ausnahmen sind:
- Video-Untertitel
- PDF

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass die Abstände zwischen Zeilen, Wörtern, Buchstaben und nach Absätzen auf die definierten Abstände angepasst werden können.

1.4.13:

In Kürze: Zusätzliche Inhalte, die angezeigt werden, wenn Elemente den Mauszeiger- oder Tastaturfokus erhalten, z.B. benutzerdefinierte Tooltips oder Fly-out-Navigationen, müssen alle folgenden drei Anforderungen erfüllen: ausblendbar, hoverbar und dauerhaft.

- Ausblendbar: Es muss eine Möglichkeit geben, einen eingeblendeten Inhalt zu schliessen, ohne den Fokus zu verschieben (z.B. durch Drücken der Escape-Taste oder durch Aktivieren desjenigen Elements, dessen Fokussierung den Inhalt einblendet).
- Hoverbar: Wenn der Mauszeiger den zusätzlichen Inhalt auslöst (Hover), dann muss dieser über den zusätzlichen Inhalt bewegt werden können, ohne dass dieser wieder verschwindet.
- Dauerhaft (persistent): Der Inhalt darf nicht selbsttätig nach einer gewissen Zeitspanne schliessen. Er muss sichtbar bleiben, bis der Hover- oder Fokus-Auslöser entfernt wurde, die Benutzerin oder der Benutzer ihn aufgehoben hat, oder seine Information nicht länger gültig ist.

Für Menschen mit Sehbehinderungen, die mit starker Zoomvergrösserung arbeiten, sind zusätzliche Inhalte, die bei Mauszeiger- oder Tastaturfokus eingeblendet werden, problematisch: 
- Aspekt «ausblendbar»: Eingeblendete Inhalte verdecken häufig andere Inhalte. Es muss möglich sein, den eingeblendeten Inhalt wieder zu schliessen, ohne den Fokus zu bewegen. Die Escape-Taste oder ein Aktivieren desjenigen auslösenden Elements (Klicken, Tippen, Enter-Taste), das zur Zeit den Fokus hat, muss den eingeblendeten Inhalt schliessen. Ausgenommen sind Fälle, bei denen der eingeblendete Inhalt eine Fehlermeldung ist oder keine anderen Inhalte verdeckt oder ersetzt.
- Aspekt «hoverbar»: Inhalte sind wegen des starken Zoomfaktors oft nur teilweise sichtbar. Es muss möglich sein, den Mauszeiger vom auslösenden Element über den eingeblendeten Inhalt zu bewegen (was meist den sichtbaren Ausschnitt verschiebt), ohne dass der eingeblendete Inhalt schliesst.
-Aspekt «dauerhaft»: Menschen mit Sehbehinderungen brauchen häufig mehr Zeit, um Inhalte zu lesen. Eingeblendete Inhalte müssen deshalb so lange zur Verfügung stehen, bis sie aktiv geschlossen werden (z.B. über Weiter-Tabben, Wegbewegen des Mauszeigers vom eingeblendetem Inhalt oder explizites Schliessen mittels Tastatur). Ausgenommen sind Fälle, bei denen der eingeblendete Inhalt nicht länger gültig ist.

Hinweise: 
- Bei Inhalten, die eingeblendet werden, wenn ein bestimmtes Element den Tastaturfokus erhält, wird nicht verlangt, dass der Mauszeiger über die eingeblendeten Inhalte bewegt werden kann, ohne dass diese sich schliessen.
- Wenn das Aktivieren (Klicken, Tippen, Enter-Taste) desjenigen Elements, das den Inhalt einblendet, zum Schliessen des eingeblendeten Inhalts führt, muss der Kontext bestehen bleiben (und darf keine weitere Aktion ausgelöst werden, die den Kontext ändert, etwa das Aktivieren eines Links).
- Wenn Inhalte durch Hover eingeblendet werden, müssen diese auch bei Tastaturfokus eingeblendet werden, ausser sie werden alternativ zur Verfügung gestellt. Für Anforderungen in Bezug auf Tastatur, beachten Sie Erfolgskriterium 2.1.1.
- Die Anforderung gilt nicht für eingeblendete Inhalte, deren Verhalten durch den Nutzer-Agenten (z.B. Browser) bestimmt wird (z.B. native title-Attribute).

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass via Hover oder Fokus eingeblendete Inhalte ausblendbar und hoverbar sind und sich nicht selbsttätig schliessen.

2.1.4:

In Kürze: Tastaturkurzbefehle mit nur einer einzelnen Taste sind für Menschen, die mit Spracheingabe (Voice Input) arbeiten, häufig problematisch. Spracheingaben können unerwartet Befehle für Funktionen auslösen. Wenn Websites Tastaturkurzbefehle über Einzeltasten (Buchstaben, Zahlen, Satzzeichen oder Symbole) implementieren, ist es deshalb essenziell, dass diese entweder deaktiviert oder auf eine Tastenkombination mit Modifikator-Taste(n) (z.B. Strg, Alt) umgestellt werden können oder dass sie für bestimmte Schnittstellen-Elemente nur aktiv sind, wenn diese den Fokus haben.

Typische Anwendungsfälle sind etwa, wenn beim Drücken von s das Suchfeld automatisch den Fokus erhält oder wenn beim Drücken von ? eine Hilfe angezeigt wird.

Beachten Sie, dass dieses Erfolgskriterium keine Auswirkungen auf Komponenten wie Listboxen und Dropdown-Menüs hat. Durch das accesskey-Attribut implementierte Tastaturkürzel sind ebenfalls nicht betroffen.

Hinweis: Einzeltasten-Kurzbefehle können auch Menschen mit motorischen Behinderungen vor Probleme stellen, insbesondere Menschen mit motorischen Behinderungen der Hände. Sie können aus Versehen Tasten drücken und damit unbeabsichtigt Aktionen auslösen. Der Nutzungskontext geht dadurch verloren.

Verantwortlichkeiten: 
- Das Entwicklungsteam stellt einen Mechanismus zur Verfügung, mit dem die Tastaturbefehle über Einzeltasten deaktiviert werden können (z.B. Umschalten-Schalter Einzeltasten-Befehle aktiv vs. Einzeltasten-Befehle deaktiviert) oder es schafft eine Möglichkeit, dass Einzeltasten-Befehle anders zugeordnet werden können.

2.5.1:

In Kürze: Zeigergesten dürfen keinen bestimmten Pfad (Streich- oder Ziehgesten) oder Mehrfach-Touch (Mehrpunktgesten) erfordern. Wenn Web-Inhalte über pfadbasierte Zeiger- oder über Mehrpunktgesten bedient werden können, muss es Alternativen geben mittels einfacher Zeigereingabe. 

Für Menschen, die in ihrer Bewegungsfreiheit stark eingeschränkt sind, ist es oft schwierig und teilweise unmöglich, Pfad- oder Mehrfach-Touch-Eingaben zu tätigen. Deshalb ist es wichtig, dass Funktionen, welche durch eben solche Eingaben ausgeführt werden, auch über eine alternative, einfach bedienbare Eingabe ausgeführt werden können (etwa einfaches Klicken, Doppelklicken, oder Klicken-und-Halten). 

Komplexe Gesten sind z.B. Streichgesten vom Rand her, um ein Menü einzublenden, Wischgesten zum Bewegen von Karussell-Inhalten, Zieh-Gesten zum Verstellen von Schiebereglern, oder Mehrpunktgesten wie die Spreizgeste zum Vergrössern eines Kartenausschnitts. Drag-and-Drop-Eingaben gelten nicht als pfadbasiert im Sinne dieses Kriteriums, denn dabei ist der Pfad zwischen Start- und Endpunkt beliebig. Ausgenommen von diesem Kriterium sind Fälle, in denen die Mehrpunkt- oder pfadbasierte Geste essenziell wichtig ist - etwa bei der Handschrifterkennung. 

Alternativen können z.B. sein:
- Das Verändern eines Kartenausschnitts ist nicht nur mit Spreizgeste möglich, sondern auch über Schalter «Karte vergrössern» bzw. «Karte verkleinern». 
- News- oder Foto-Slider können nicht nur mittels Wischgeste bewegt werden, sondern auch über Pfeiltasten nach links und nach rechts für die weiteren Elemente. 
- In einem Projektmanagement-Werkzeug mit diversen Spalten können die Arbeitspakete nicht nur mittels Wischgeste in eine andere Spalte verschoben werden, sondern auch indem man ein Element markiert und es mit Pfeilen in die andere Spalte verschiebt.

Hinweis: 'Zeiger' meint in diesem Kontext indirekte Eingaben mittels Mauszeiger ebenso wie direkte Eingaben, etwa mit dem Finger auf dem Touchscreen oder mit dem Stift auf einem Tablet.

Wichtig: Diese Anforderung gilt nur für Zeigergesten, die von Web-Inhalten interpretiert und verarbeitet werden - sie betreffen also nicht Gesten für die Bedienung von Nutzeragenten oder Hilfsmitteln (z.B. Gesten zur Navigation zwischen Seiten im Browser oder Gesten zur Nutzung systemseitiger Screenreader).

Verantwortlichkeiten: 
- Das Entwicklungsteam stellt Alternativen zur Verfügung, wenn Mehrpunkt- oder pfadbasierte Gesten für die Bedienung von Web-Inhalten implementiert werden.

2.5.2:

In Kürze: Um das Risiko zu minimieren, dass Funktionalitäten versehentlich ausgeführt werden, müssen Zeigereingaben noch während der Eingabe abgebrochen werden können oder es muss möglich sein, sie rückgängig zu machen.

Drückt beispielsweise ein an Tremor leidender Nutzer aus Versehen den falschen Schalter (etwa «Anruf beenden» anstelle von «Stumm schalten»), so kann er die Eingabe normalerweise abbrechen, indem er den Finger vom Schalter weg bewegt und erst dann hoch hebt (und somit verhindert, dass die Aktion ausgelöst wird).

Funktionalität, welche mit einem Zeigegerät bedient wird, muss mindestens einen der folgenden Punkte erfüllen:
- Kein Down-Event: Der Down-Event wird gar nicht genutzt, um die Funktion (oder einen Teil derselben) auszulösen.
- Abbrechen oder rückgängig machen: Die Funktion wird beim Up-Event ausgelöst, und es steht ein Mechanismus zur Verfügung, um die Funktion vor dem Ausführen abzubrechen oder die Funktion nach dem Ausführen rückgängig zu machen.
- Umkehrung bei Up: Der Up-Event kehrt jegliche Auswirkung des vorangehenden Down-Events um. Beispiel: Jemand hält die «Abspielen»-Schaltfläche eines Video-Players gedrückt, was das Abspielen des Videos startet, und hört dann auf zu drücken, was das Abspielen wieder stoppt. Dadurch kehrt man zu m Ausgangspunkt zurück und hat den Vorgang effektiv abgebrochen.
- Essenziell: Das Ausführen der Funktion auf dem Down-Event ist unerlässlich. Beispiel: Zeichnen mittels Maus, Eingabestift oder Finger auf einem Touchscreen; Interagieren mit einer virtuellen Tastatur; Emulieren eines physischen Tastendrucks (z.B. in einer Musik-Applikation, die eine Klaviertastatur anbietet).

Hinweis: 
- Für komplexere Interaktionen, z.B. Drag-and-Drop, steigt die Notwendigkeit für eine Abbruch- oder Rückgängig-Funktion.
- Wenn die Funktion nach dem Ausführen durch einen Dialog bestätigt werden muss, dann entfällt die Notwendigkeit für eine Rückgängig-Funktion.
- Unter Up-Event versteht man das Ausführen einer Aktion, wenn der Zeiger losgelassen wird, also die Maustaste losgelassen bzw. auf einem Touchscreen der Finger angehoben wird. Als Down-Events gelten mousedown, touchstart und pointerdown.

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass die Vorgaben für Zeigereingaben-Abbrüche umgesetzt werden. Empfohlen sind Standard-HTML-Elemente und Click-Events, während Up-Events wenn möglich vermieden werden sollten.

2.5.3:

In Kürze: Via Spracheingabe können Bedienelemente wie Links, Schalter, Checkboxen oder Eingabefelder gesteuert werden, indem die sichtbare Beschriftung gesprochen wird. Das funktioniert auch in der Verbindung mit Befehlen (z.B. «Klicke 'Anmelden'»). Die für assistierende Technologien verfügbare Beschriftung eines Bedienelements muss gleich sein wie die visuell sichtbare Beschriftung oder diese enthalten. Ist das nicht der Fall, ist die Bedienung z.B. mittels Sprachsteuerung nicht oder nur auf Umwegen möglich.

Bei Bedienelementen mit Beschriftungen, die Text oder Bilder von Text enthalten, enthält der zugängliche Name den sichtbaren Text. Manchmal wird versteckter Text benutzt, um sichtbare Beschriftungen zu erweitern, oft auch in der Absicht, Menschen mit Behinderungen zu helfen. Das ist zulässig, wenn die sichtbare Beschriftung durchgehend im zugänglichen Namen enthalten ist, am besten zu Beginn.

Problematisch sind z.B. grafische Schalter mit visuell sichtbarem Label, bei denen die Textalternative nicht genau dem visuellen Label entspricht. Dadurch wird eine Sprachsteuerung verunmöglicht, weil das System in der Folge nicht auf das visuelle Label reagiert. Die sichtbare Beschriftung «AGB akzeptieren» einer Checkbox könnte z.B. im hinterlegten zugänglichen Namen durch «Allgemeine Geschäftsbedingungen annehmen» ersetzt werden. Wenn via Spracheingabe nun «Klicke 'AGB akzeptieren'» diktiert wird, ist dieser Text so nicht im zugänglichen Namen enthalten und die Eingabe schlägt fehl.

Die zugängliche Beschriftung kann von der sichtbaren Beschriftung abweichen, wenn sie z.B. über nicht sichtbare Attribute festgelegt wird: alt-Attribute bei Grafiken, <label>-Elemente, Attribute wie aria-label und aria-labelledby (aria-describedby hingegen nicht), etc. Dabei ist zu beachten, dass sowohl aria-label als auch aria-labelledby ein ebenfalls vorhandenes HTML-Label überschreiben.

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass Bedienelemente, die fix programmiert werden, die Vorgaben erfüllen. Dabei muss die sichtbare Zeichenkette vollständig und genau in der zugänglichen Beschriftung enthalten sein. Zusätzliche Texte innerhalb dieser Zeichenketten sind unzulässig.
- Die Inhaltsverantwortlichen verfassen Beschriftungen für von ihnen erstellte Bedienelemente (z.B. Anmelden-Schalter in einem Formular) so, dass die sichtbare Beschriftung vollständig und genau auch im Code enthalten ist. Bietet das CMS keine Option, separat zugängliche Beschriftungen zu erfassen, liegt die Verantwortlichkeit allein beim Entwicklungsteam.
"

2.5.4:

In Kürze: Funktionalität, die durch Gerätebewegung (etwa Schütteln des Geräts) ausgelöst wird, muss ebenfalls über eine alternative, einfach bedienbare Eingabe ausgeführt werden können. Es darf nicht vorausgesetzt werden, dass alle Geräte bewegt werden können, z.B. bei einem an einem Rollstuhl befestigten Smartphone (physisch in einer Halterung verankert). Ausserdem muss eine solche Funktionalität deaktiviert werden können, damit sie nicht aus Versehen ausgelöst wird, z.B. Schüttelbewegung aufgrund von Muskelzittern (Tremor).

Eine Ausnahme bilden Bewegungseingaben, die für die Funktion wesentlich sind und notwendigerweise auf Gerätesteuerung basieren, z.B. wenn ein Bewegungssensor die Schritte einer Person aufzeichnet oder wenn die Bewegung Teil einer zugänglichkeitsunterstützten Hilfsmitteleingabe ist.

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass Alternativen bestehen für Funktionen, die über Geräte- oder Benutzerbewegung ausgelöst werden können. Ausserdem müssen solche Funktionalitäten deaktiviert werden können.

4.1.3:

In Kürze: Statusmeldungen liefern Informationen über Erfolg, Fortschritt oder Ergebnis einer Aktion, oder auch über auftretende Fehler. Gleichzeitig wird der Fokus dabei nicht neu gesetzt (z.B. durch Neuladen der Seite o.ä.). Da assistierende Technologien (z.B. Screenreader) nicht immer den ganzen Seiteninhalt überwachen, sind in diesen Fällen spezielle Massnahmen erforderlich, damit diese Statusmeldungen trotzdem ausgegeben werden.

Wenn Statusmeldungen erzeugt werden, z.B. Fehlermeldungen, Bestätigungsmeldungen, Ladenanzeigen/Fortschrittsbalken, etc., müssen visuell eingeblendete Statusmeldungen über geeignete Rollen oder Eigenschaften so ausgezeichnet werden, dass sie auch programmiertechnisch ermittelbar sind und mittels assistierender Technologien ausgegeben werden.

Folgende Meldungen müssen z.B. in einem Screenreader ausgegeben werden, ohne dass der Fokus auf sie gesetzt wird:
-  «27 Ergebnisse gefunden», z.B. wenn ein Filter angepasst wird und automatisch die Suchergebnisse aktualisiert werden.
- «Bitte warten Sie», «Seite wird geladen», z.B. nach dem Absenden einer Suchanfrage.
- «Persönliches Profil erfolgreich gespeichert», z.B. nach Aktualisieren und Speichern von Angaben in einem persönlichen Profil.
- «2 Produkte im Warenkorb», «Produkt in den Warenkorb gelegt», z.B. wenn per Schaltfläche die Zahl der Produkte in einem Warenkorb erhöht wird oder ein Produkt dem Warenkorb hinzugefügt wird.
- «Buch auf der Merkliste ergänzt», z.B. wenn eine Merken-Funktion für Produkte zur Verfügung steht.
- «3 Felder sind fehlerhaft», z.B. bei clientseitiger Überprüfung eines Formulars ohne Neuladen der Seite
- etc.

Hinweis: Eine Ausgabe durch assistierende Technologien auch ohne Fokussetzung kann durch Verwendung von ARIA role="alert" oder mittels Live Regions erfolgen.

Verantwortlichkeiten:
- Das Entwicklungsteam stellen sicher, dass Statusmeldungen so implementiert sind, dass sie von assistierenden Technologien (z.B. Screenreadern) automatisch erkannt und ausgegeben werden können.
