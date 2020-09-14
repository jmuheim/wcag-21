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

---

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

---

2.5.3:

In Kürze: Via Spracheingabe können Bedienelemente wie Links, Schalter, Checkboxen oder Eingabefelder gesteuert werden, indem die sichtbare Beschriftung gesprochen wird. Das funktioniert auch in der Verbindung mit Befehlen (z.B. «Klicke 'Anmelden'»). Die für assistierende Technologien verfügbare Beschriftung eines Bedienelements muss gleich sein wie die visuell sichtbare Beschriftung oder diese enthalten. Ist das nicht der Fall, ist die Bedienung z.B. mittels Sprachsteuerung nicht oder nur auf Umwegen möglich.

Bei Bedienelementen mit Beschriftungen, die Text oder Bilder von Text enthalten, enthält der zugängliche Name den sichtbaren Text. Manchmal wird versteckter Text benutzt, um sichtbare Beschriftungen zu erweitern, oft auch in der Absicht, Menschen mit Behinderungen zu helfen. Das ist zulässig, wenn die sichtbare Beschriftung an einem Stück im zugänglichen Namen enthalten ist, am besten zu Beginn.

Problematisch sind z.B. grafische Schalter mit visuell sichtbarem Label, bei denen die Textalternative nicht genau dem visuellen Label entspricht. Dadurch wird eine Sprachsteuerung verunmöglicht, weil das System in der Folge nicht auf das visuelle Label reagiert. Die sichtbare Beschriftung «AGB akzeptieren» einer Checkbox könnte z.B. im hinterlegten zugänglichen Namen durch «Allgemeine Geschäftsbedingungen annehmen» ersetzt werden. Wenn via Spracheingabe nun «Klicke 'AGB akzeptieren'» diktiert wird, ist dieser Text so nicht im zugänglichen Namen enthalten und die Eingabe schlägt fehl.

Die zugängliche Beschriftung kann von der sichtbaren Beschriftung abweichen, wenn sie z.B. über nicht sichtbare Attribute festgelegt wird: alt-Attribute bei Grafiken, <label>-Elemente, Attribute wie aria-label und aria-labelledby (aria-describedby hingegen nicht), etc. Dabei ist zu beachten, dass sowohl aria-label als auch aria-labelledby ein ebenfalls vorhandenes HTML-Label überschreiben.

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass Bedienelemente, die fix programmiert werden, die Vorgaben erfüllen. Dabei muss die sichtbare Zeichenkette vollständig und genau in der zugänglichen Beschriftung enthalten sein. Zusätzliche Texte innerhalb dieser Zeichenketten sind unzulässig.
- Die Inhaltsverantwortlichen verfassen Beschriftungen für von ihnen erstellte Bedienelemente (z.B. Anmelden-Schalter in einem Formular) so, dass die sichtbare Beschriftung vollständig und genau auch im Code enthalten ist. Bietet das CMS keine Option, separat zugängliche Beschriftungen zu erfassen, liegt die Verantwortlichkeit allein beim Entwicklungsteam.

---

2.5.4: In Kürze: Funktionalität, die durch Gerätebewegung (etwa Schütteln des Geräts) ausgelöst wird, muss ebenfalls über eine alternative, einfach bedienbare Eingabe ausgeführt werden können. Es darf nicht vorausgesetzt werden, dass alle Geräte bewegt werden können, z.B. bei einem an einem Rollstuhl befestigten Smartphone (physisch in einer Halterung verankert). Ausserdem muss eine solche Funktionalität deaktiviert werden können, damit sie nicht aus Versehen ausgelöst wird, z.B. Schüttelbewegung aufgrund von Muskelzittern (Tremor).

Eine Ausnahme bilden Bewegungseingaben, die für die Funktion wesentlich sind und notwendigerweise auf Gerätesteuerung basieren, z.B. wenn ein Bewegungssensor die Schritte einer Person aufzeichnet oder wenn die Bewegung Teil einer zugänglichkeitsunterstützten Hilfsmitteleingabe ist.

Verantwortlichkeiten:
- Das Entwicklungsteam stellt sicher, dass Alternativen bestehen für Funktionen, die über Geräte- oder Benutzerbewegung ausgelöst werden können. Ausserdem müssen solche Funktionalitäten deaktiviert werden können.

---

4.1.3:

In Kürze: Statusmeldungen liefern Informationen über Erfolg, Fortschritt oder Ergebnis einer Aktion, oder auch über auftretende Fehler. Gleichzeitig wird der Fokus dabei nicht neu gesetzt (z.B. durch Neuladen der Seite o.ä.). Da assistierende Technologien (z.B. Screenreader) nicht immer den ganzen Seiteninhalt überwachen, sind in diesen Fällen spezielle Massnahmen erforderlich, damit diese Statusmeldungen trotzdem ausgegeben werden.

Wenn Statusmeldungen erzeugt werden, z.B. Fehlermeldungen, Bestätigungsmeldungen, Ladeanzeigen/Fortschrittsbalken, etc., müssen visuell eingeblendete Statusmeldungen über geeignete Rollen oder Eigenschaften so ausgezeichnet werden, dass sie auch programmiertechnisch ermittelbar sind und mittels assistierender Technologien ausgegeben werden.

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
