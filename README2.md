2.5.1:

In Kürze: Für Web-Inhalte, die über pfadbasierte Zeiger- oder über Mehrpunktgesten bedient werden, muss es alternative Eingabemöglichkeiten geben mittels einfacher Zeigereingabe. Dies ermöglicht Menschen, die in ihrer Bewegungsfreiheit eingeschränkt sind, jene Inhalte ebenfalls zu bedienen.

Für Menschen, die in ihrer Bewegungsfreiheit stark eingeschränkt sind, ist es oft schwierig und teilweise unmöglich, Pfad- oder Mehrfach-Touch-Eingaben zu tätigen.  Komplexe Gesten sind z.B. Streichgesten vom Rand her, um ein Menü einzublenden, Wischgesten zum Bewegen von Karussell-Inhalten, Zieh-Gesten zum Verstellen von Schiebereglern, oder Mehrpunktgesten wie die Spreizgeste zum Vergrössern eines Kartenausschnitts. Drag-and-Drop-Eingaben gelten nicht als pfadbasiert im Sinne dieses Kriteriums, denn dabei ist der Pfad zwischen Start- und Endpunkt beliebig.

Deshalb ist es wichtig, dass Funktionen, welche durch eben solche Eingaben ausgeführt werden, auch über eine alternative, einfach bedienbare Eingabe ausgeführt werden können (etwa einfaches Klicken, Doppelklicken, oder Klicken-und-Halten). Alternativen können z.B. sein:

- Das Verändern eines Kartenausschnitts ist nicht nur mit Spreizgeste möglich, sondern auch über Schalter "Karte vergrössern" bzw. "Karte verkleinern". 
- News- oder Foto-Slider können nicht nur mittels Wischgeste bewegt werden, sondern auch über Pfeiltasten nach links und nach rechts für die weiteren Elemente. 
- In einem Projektmanagement-Werkzeug mit diversen Spalten können die Arbeitspakete nicht nur mittels Wischgeste in eine andere Spalte verschoben werden, sondern auch indem man ein Element markiert und es mit Pfeilen in die andere Spalte verschiebt.

Ausnahmen: Ausgenommen von diesem Kriterium sind Fälle, in denen die Mehrpunkt- oder pfadbasierte Geste essenziell wichtig ist - etwa bei der Handschrifterkennung. 

Hinweis: "Zeiger" meint in diesem Kontext indirekte Eingaben mittels Mauszeiger ebenso wie direkte Eingaben, etwa mit dem Finger auf dem Touchscreen oder mit dem Stift auf einem Tablet.

Wichtig: Diese Anforderung gilt nur für Zeigergesten, die von Web-Inhalten interpretiert und verarbeitet werden - sie betreffen also nicht Gesten für die Bedienung von Nutzeragenten oder Hilfsmitteln (z.B. Gesten zur Navigation zwischen Seiten im Browser oder Gesten zur Nutzung systemseitiger Screenreader).

Verantwortlichkeiten:

- Das Entwicklungsteam stellt alternative Bedienungsmöglichkeiten zur Verfügung, wenn Mehrpunkt- oder pfadbasierte Gesten für die Bedienung von Web-Inhalten implementiert werden.

---

2.5.2:

In Kürze: Zeigereingaben müssen noch während der Eingabe abgebrochen werden können, oder es muss möglich sein, sie rückgängig zu machen. Dies ermöglicht das Abbrechen von unbeabsichtigten Eingaben, wodurch das Risiko minimiert wird, dass Funktionalitäten versehentlich ausgeführt werden.

Diverse Behinderungsformen schränken die Präzision von Eingaben während der Benutzung von Geräten ein, wodurch es zu Falscheingaben kommen kann. Drückt beispielsweise ein an Muskelzittern (Tremor) leidender Mensch aus Versehen den falschen Schalter (etwa "Anruf beenden" anstelle von "Stumm schalten"), so kann er die Eingabe normalerweise noch abbrechen, indem er den Finger vom Schalter weg bewegt und erst dann hoch hebt (und somit verhindert, dass die Aktion ausgelöst wird).

Deshalb muss Funktionalität, welche mit einem Zeigegerät bedient wird, mindestens einen der folgenden Punkte erfüllen:

- Kein Down-Event: Der Down-Event wird gar nicht genutzt, um die Funktion (oder einen Teil derselben) auszulösen.
- Abbrechen oder rückgängig machen: Die Funktion wird beim Up-Event ausgelöst, und es steht ein Mechanismus zur Verfügung, um die Funktion vor dem Ausführen abzubrechen oder die Funktion nach dem Ausführen rückgängig zu machen.
- Umkehrung bei Up: Der Up-Event kehrt jegliche Auswirkung des vorangehenden Down-Events um. Beispiel: Jemand hält die "Abspielen"-Schaltfläche eines Video-Players gedrückt, was das Abspielen des Videos startet, und hört dann auf zu drücken, was das Abspielen wieder stoppt. Dadurch kehrt man zum Ausgangspunkt zurück und hat den Vorgang effektiv abgebrochen.
- Essenziell: Das Ausführen der Funktion auf dem Down-Event ist unerlässlich. Beispiel: Zeichnen mittels Maus, Eingabestift oder Finger auf einem Touchscreen; Interagieren mit einer virtuellen Tastatur; Emulieren eines physischen Tastendrucks (z.B. in einer Musik-Applikation, die eine Klaviertastatur anbietet).

Hinweise:

- Für komplexere Interaktionen, z.B. Drag-and-Drop, steigt die Notwendigkeit für eine Abbruch- oder Rückgängig-Funktion.
- Wenn die Funktion nach dem Ausführen durch einen Dialog bestätigt werden muss, dann entfällt die Notwendigkeit für eine Rückgängig-Funktion.
- Unter Up-Event versteht man das Ausführen einer Aktion, wenn der Zeiger losgelassen wird, also die Maustaste losgelassen bzw. auf einem Touchscreen der Finger angehoben wird. Als Down-Events gelten mousedown, touchstart und pointerdown.

Verantwortlichkeiten:

- Das Entwicklungsteam stellt sicher, dass die Vorgaben für Zeigereingaben-Abbrüche umgesetzt werden. Empfohlen sind Standard-HTML-Elemente und Click-Events, während Down-Events wenn möglich vermieden werden sollten.

---

2.5.3:

In Kürze: Die für assistierende Technologien (z.B. Screenreader) verfügbare Beschriftung eines Bedienelements muss gleich sein wie die visuell sichtbare Beschriftung, oder sie muss diese enthalten. Dies ermöglicht Menschen, welche die Bedienelemente visuell sehen, aber z.B. über eine Sprachsteuerung mit ihnen interagieren, die intuitive Bedienung derselben.

Via Spracheingabe können Bedienelemente wie Links, Schalter, Checkboxen oder Eingabefelder gesteuert werden, indem die sichtbare Beschriftung gesprochen wird. Das funktioniert auch in der Verbindung mit Befehlen (z.B. "Klicke Anmelden"). Unterscheidet sich die visuell sichtbare Beschriftung aber von der zugänglichen Beschriftung, ist die Bedienung z.B. mittels Sprachsteuerung nicht oder nur auf Umwegen möglich.

Bei Bedienelementen mit Beschriftungen, die Text oder Bilder von Text enthalten, muss der zugängliche Name den sichtbaren Text enthalten. Manchmal wird versteckter Text benutzt, um sichtbare Beschriftungen zu erweitern, oft auch in der Absicht, Menschen mit Behinderungen zu helfen. Das ist zulässig, wenn die sichtbare Beschriftung an einem Stück im zugänglichen Namen enthalten ist, am besten zu Beginn.

Problematisch sind z.B. grafische Schalter mit visuell sichtbarem Label, bei denen die Textalternative nicht genau dem visuellen Label entspricht. Dadurch wird eine Sprachsteuerung verunmöglicht, weil das System in der Folge nicht auf das visuelle Label reagiert. Die sichtbare Beschriftung "AGB akzeptieren" einer Checkbox könnte z.B. im hinterlegten zugänglichen Namen durch "Allgemeine Geschäftsbedingungen annehmen" ersetzt werden. Wenn via Spracheingabe nun "Klicke AGB akzeptieren" diktiert wird, ist dieser Text so nicht im zugänglichen Namen enthalten und die Eingabe schlägt fehl.

Die zugängliche Beschriftung kann von der sichtbaren Beschriftung abweichen, wenn sie z.B. über nicht sichtbare Attribute festgelegt wird: alt-Attribute bei Grafiken, visuell versteckte (oder visuell nicht eindeutig zuweisbare) <label>-Elemente, Attribute wie aria-label und aria-labelledby (aria-describedby hingegen nicht), etc. Dabei ist zu beachten, dass sowohl aria-label als auch aria-labelledby ein ebenfalls vorhandenes HTML-Label überschreiben.

Verantwortlichkeiten:

- Das Entwicklungsteam stellt sicher, dass Bedienelemente, die fix programmiert werden, die Vorgaben erfüllen. Dabei muss die sichtbare Zeichenkette vollständig und genau in der zugänglichen Beschriftung enthalten sein. Zusätzliche Texte innerhalb dieser Zeichenketten sind unzulässig.
- Die Inhaltsverantwortlichen verfassen Beschriftungen für von ihnen erstellte Bedienelemente (z.B. Anmelden-Schalter in einem Formular) so, dass die sichtbare Beschriftung vollständig und genau auch im Code enthalten ist. Bietet das CMS keine Option, separat zugängliche Beschriftungen zu erfassen, liegt die Verantwortlichkeit allein beim Entwicklungsteam.

---

2.5.4:

In Kürze: Funktionalität, die durch Gerätebewegung (etwa Schütteln des Geräts) ausgelöst wird, muss ebenfalls über eine alternative, einfach bedienbare Eingabe ausgeführt werden können; ausserdem muss eine solche Funktionalität deaktiviert werden können. Dies ermöglicht motorisch eingeschränkten Menschen, jene Funktionalitäten bei Bedarf auch zu nutzen.

Motorisch stark eingeschränkte Menschen, können ihr Gerät nicht beliebig (oder gar nicht) bewegen, z.B. weil ihr Smartphone an einem Rollstuhl befestigt ist (physisch in einer Halterung verankert). Es darf also nicht vorausgesetzt werden, dass alle Geräte bewegt werden können.

Zudem muss sicher gestellt sein, dass solche Funktionalitäten nicht aus Versehen ausgelöst werden, z.B. durch eine Schüttelbewegung aufgrund von Muskelzittern (Tremor). Sie müssen deshalb deaktivierbar sein.

Ausnahme: Bewegungseingaben, die für die Funktion wesentlich sind und notwendigerweise auf Gerätesteuerung basieren, z.B. wenn ein Bewegungssensor die Schritte einer Person aufzeichnet oder wenn die Bewegung Teil einer zugänglichkeitsunterstützten Hilfsmitteleingabe ist.

Verantwortlichkeiten:

- Das Entwicklungsteam stellt sicher, dass Alternativen bestehen für Funktionen, die über Geräte- oder Benutzerbewegung ausgelöst werden können. Ausserdem müssen solche Funktionalitäten deaktiviert werden können.

---

4.1.3:

In Kürze: Statusmeldungen (Informationen über Erfolg, Fortschritt oder Ergebnis einer Aktion, oder auch über auftretende Fehler) müssen von assistierenden Technologien (z.B. Screenreader) erkannt werden können. Dies erlaubt die automatische Ausgabe jener Meldungen, ohne dass sie manuell gesucht werden müssen und potenziell übersehen werden.

Da assistierende Technologien (z.B. Screenreader) nicht immer den ganzen Seiteninhalt überwachen, sind in Fällen, wo sich ein Teil der aktuellen Seite ändert (z.B. um eine Fehlermeldung anzuzeigen), spezielle Massnahmen erforderlich, damit diese Änderungen trotzdem ausgegeben werden, und ohne dass der Fokus dabei neu gesetzt wird (z.B. durch Neuladen der Seite o.ä.).

Wenn Statusmeldungen visuell eingeblendet werden (z.B. Fehlermeldungen, Bestätigungsmeldungen, Ladeanzeigen/Fortschrittsbalken, etc.), müssen diese über geeignete Rollen oder Eigenschaften so ausgezeichnet werden, dass sie auch programmiertechnisch ermittelbar sind und mittels assistierender Technologien ausgegeben werden können.

Folgende Meldungen müssen z.B. in einem Screenreader ausgegeben werden, ohne dass der Fokus auf sie gesetzt wird:

-  "27 Ergebnisse gefunden", z.B. wenn ein Filter angepasst wird und automatisch die Suchergebnisse aktualisiert werden.
- "Bitte warten Sie", "Seite wird geladen", z.B. nach dem Absenden einer Suchanfrage.
- "Persönliches Profil erfolgreich gespeichert", z.B. nach Aktualisieren und Speichern von Angaben in einem persönlichen Profil.
- "2 Produkte im Warenkorb", "Produkt in den Warenkorb gelegt", z.B. wenn per Schaltfläche die Zahl der Produkte in einem Warenkorb erhöht wird oder ein Produkt dem Warenkorb hinzugefügt wird.
- "Buch auf der Merkliste ergänzt", z.B. wenn eine Merken-Funktion für Produkte zur Verfügung steht.
- "3 Felder sind fehlerhaft", z.B. bei clientseitiger Überprüfung eines Formulars ohne Neuladen der Seite

Tipp: Eine Ausgabe durch assistierende Technologien auch ohne Fokussetzung kann durch Verwendung von ARIA role="alert" oder mittels Live Regions erfolgen. Setzen Sie diese aber sorgfältig ein, um den Audiokanal nicht zu überstrapazieren.

Verantwortlichkeiten:

- Das Entwicklungsteam stellt sicher, dass Statusmeldungen so implementiert sind, dass sie von assistierenden Technologien (z.B. Screenreadern) automatisch erkannt und ausgegeben werden können.
