# Auszeichnungsmethode

Stand März 2025

Dass die Grundbuch-Einträge grob einem Formular folgen, ist seit längerem bekannt. Die Idee, dies als Formular-Ansicht für eine Grundbuch-Edition umzusetzen, ist jedoch neu. Wir nennen die Formular-Ansicht und die Markierungen der Formular-Slots deshalb das _Berliner Modell_. 

Grundlage für die Formular-Ansicht ist so weit wie möglich die _intendierte Textgestalt_. In der normalen Ansicht verwenden wir `<unclear>`, wenn etwas nicht sicher zu lesen ist, und `<del>`, wenn etwas vom Schreiber direkt beim Schreiben durchgestrichen wurde. In der Formular-Ansicht sind unklare Stelle in Klammern, durchgestrichene Stellen sind ganz weggelassen.

## Formular-Ansicht

Der Text jedes Eintrags wird in seine Formular-Slots aufgeteilt und die jeweiligen Rollen der Slots markiert. Ein einfaches Beispiel aus dem Kaufbuch E ist [KB-E 013-2](../edition/KB-E.xml?id=img_013):

```
ⓋAgnes von Lincz
Ⓔhat verkaufft

Ⓞain haus
Ⓛgelegen vor Widmertor ze Wienn
Ⓝzenegst Jacobin der Paugkerin haus

Ⓟumb vier und zwainczig phunt Wienner phenning
Ⓐdem erbern mann Veiten dem Valkchner 
und frawn Barbaren seiner hausfrawn

und ir baider erben
furbaser ledichlich und freileich zehaben 
und allen irn frumen damit zeschaffen

ut littera sonat 
ⒹActum an Freitag vor Bartholomei Anno domini Mº ccccº xxiiº
Summa xlviii d.
```

Alle für uns relevanten Formularteile werden markiert, nicht weiter ausgewertete Stellen können auch unmarkiert bleiben. 

### Reihenfolge der Slots

Die Reihenfolge der Slots variiert. Ein grundlegender Unterschied ist zwischen Kaufbuch und Gewerbüchern: 
* Kaufbuch: Agnes verkauft ein Objekt (mit Lage und Nachbarn) an Veit und Barbara
* Gewerbücher: Veit und Barbara erhalten ein Objekt (mit Lage und Nachbarn) mit Kauf von Agnes

Aber auch darüber hinaus ist die Reihenfolge nicht fix. Die Daten-Auswertung muss damit umgehen können.

## Übersicht über die Formular-Slots

Ein Slot kann mit einem _circled capital letter_ (Ⓐ bis Ⓩ) oder einem _circled small letter_ (ⓐ bis ⓩ) markiert werden. Als Faustregel wird alles, was danach ausgewertet wird, mit einem Großbuchstaben markiert, und alles andere mit einem Kleinbuchstaben.

### Objekte

Ein Eintrag handelt meistens, aber nicht immer, von einem einzigen Objekt. Meistens geht es um ein Haus, aber manchmal auch um eine Fleischbank etc. Oft geht es nur um einen Hausteil. 

| Slot |Beispiel |
|:-----|:--------|
| Objekt | Ⓞains hawss |
| Lage | Ⓛgelegen in der Weyhenpurgk |
| Nachbarhaus | Ⓝzenagst Veyten des Illuminator <br/>Ⓝund Erharten des Tuchbraiter hewser |
| Hausteilung | Ⓣdes ettwen zway hewser gewesen sein |
| Hausname | Ⓒgenant des Ketner haus |
| zusätzlich | ⓜmitsambt dem hoflein daz besunder darczu kaufft ist |

#### Belastungen auf dem Haus

Belastungen auf den Grundstücken/Immobilien durch z.B. Erbzins oder Nießbrauchrechte, insbesondere Burgrecht und Grunddienst. Default ist Ⓑ.


| Slot |Beispiel |
|:-----|:--------|
| Burgrecht<br/>bzw. Hypothek | Ⓑ davon man Jerlichen dint <br/>hincz sand Larenczen ze Wienn <br/>iiii tl. d. ze purkrecht |
| | (Ⓠ speziell für Grunddienst) |
| Burgrecht-Ende | ⓑund nicht mer | 

### Ereignisse

| Slot |Beispiel |
|:-----|:--------|
| Zustand | Ⓩ x |
| Ereignistyp | Ⓔ x |
| von | Ⓥ x |
| an | ⒶAgnes Petern des Schellen seligen wittib |
| Empfangen-Floskel | ⓗhat emphangen nucz und gwer |
| Kaufpreis | Ⓟ x |
| Datum | Ⓓ x |
| Eintragungsgebühr | ⓟ x |

Ⓓ bezeichnet damit das Haupt-Datum des Eintrags.

Ⓟ steht für einen Kaufpreis, ⓟ steht für die Eintragungsgebühr.

ⓐ war ein Versuch, zwischen echtem Käufer/Verkäufer und den Durchführenden des Rechtsgeschäfts zu unterscheiden:

```
ⒶDorothe 
Casparn Cirnos und Margrethen seiner hausfrawn die vormaln Giligen Winkhl seligen auch elichen gehabt hat seligen tochter 
ⓐist durch die erbern Linharten Rorer und Hannsen Grurber Ir Gerhaben 
ⓗnucz und gwer pracht worden 
```

ⓔ für "Neben-Ereignisse"

Mögliche zukünftige Ereignisse wie "falls sich noch Erben melden" werten wir nicht aus.

### Notizen

| Slot |Beispiel |
|:-----|:--------|
| nachträgliche Notiz | Ⓗ x |
| Datumsangabe in der Notiz | ⓓ x |

Ⓓ bezeichnet damit ein Neben-Datum im Eintrag.

### Urkunden-Floskeln 

Markierungen für Floskeln und anderes Slots, die wir nicht weiter auswerten, sind eher experimentell und nicht systematisch eingetragen. Wir sind uns noch nicht sicher, ob es hilft (und den Aufwand lohnt) oder ob es den Text nur schwerer lesbar macht. Eventuell reicht eine einzige Markierung für alle Floskeln, oder sie werden gar nicht markiert.

| Slot |Beispiel |
|:-----|:--------|
| Urkunden-Floskel | ⓤut littera sonat |


### verschiedenes

| Slot |Beispiel |
|:-----|:--------|
| Klauseln, die wir nicht auswerten | Ⓧ x |
| moderne Kommentare | Ⓚ x |


rechtliche Details des Hausbesitzes:
```
erⓣdoch also daz der egenant Kuncz alczeit ganczen gewalt sol haben mit dem egenant haws allen seinen frumen zuschaffen 
ⓢfurbaser allen Irn frumen damit zeschaffen wie sew verlusst 
```

Die neuen Eigentümer können mit dem Haus machen, was sie wollen. Insbesondere liegen keine Hypotheken auf dem Haus.

```
ⒶMicheln dem freisleben ze Wienn Margrethen seiner hausfraw
ⓡund ir baider erben
ⓠoder welchs under in baiden das ander uberlebt
```

Erbregelung

## Entscheidungen bei der Formular-Ansicht

Nur ein kleiner Teil der Einträge folgt dem Schema perfekt. Die genaue Einteilung hängt auch davon ab, was dem Lesefluss nützt. Zum Beispiel wird in den Gewerbüchern das Objekt oft wieder aufgenommen. Eine komplexe Wiederaufnahme wie "als dasselb halb haws" (GB-D 0052-6) bekommt eine eigene Zeile:

```
ⒶAndre Kelhaimer burger zu Wienn 
ⓗhat emphangen nucz und gewer 

Ⓞains halben hawss 
Ⓛganczes gelegen undern fleischpenkchen 
Ⓝam placz zenagst des Angerfelder haws 
```

```
als dasselb halb haws 
mit allen gemechen und gemainen stukchen die nach lautt der tailbrief darczu gehornt 
Ⓟumb funfczehen hundert phunt phenning 
Ⓥvon Hainreichen Frankchen seinem swager 
Ⓔmit kauf an In komen ist 
nach lautt ains kaufbriefs den er darumb hat 
```

Ein einfaches "als das" wird dagegen einfach in einen anderen Formular-Slot integriert:

```
ⒶAndre Kelhaimer Burger zu Wienn 
ⓗhat emphangen nucz und gewer 

Ⓞains hawss 
Ⓛgelegen in der vodern Pekchenstrazz 
Ⓝzenagst Wolfgangs Hertting haws 
```

```
Als daz von dem Erwurdigen geistlichen herren hern Wolfgangen Abt und seinem Convent des gaczhauss zu Pawmgartenstern 
Ⓟumb virdhalb hundert phunt phenning 
Ⓔmit kauf an In komen ist 
```

Ein Problem ist daher, dass die Semantik der Zeilenumbrüche nicht immer einheitlich und damit für ein Skript nicht immer verständlich ist. Manchmal sind sie nur da, um es für Menschen lesbarer zu machen. Wir arbeiten noch an einem Kompromiss zwischen Lesbarkeit für Menschen und automatischer Auswertbarkeit. Zum Beispiel kann ein Skript die Wiederaufnahme 

```
als dasselb halb haws 
mit allen gemechen und gemainen stukchen die nach lautt der tailbrief darczu gehornt 
```

einfach ignorieren. Das ist für das Skript auch leicht erkennbar, weil die Zeilen direkt nach einer Leerzeile stehen und keine Markierung haben.

## Normalisierung, kontrolliertes Vokabular und IDs

Links von einer Markierung kann noch hinzugefügter Text stehen:
* Normalisierungen 
* kontrolliertes Vokabular
* IDs

Beachte: Bei Burgrecht sind die enthaltenen Orte und Personen sowie die Summen sind noch nicht markiert. Für uns hat ein Burgrecht bisher nur die Funktion, dass es bei der Entscheidung hilft, ob zwei Einträge vom selben Haus sprechen, und wenn man Hauspreise analysiert, muss man die Hypotheken berücksichtigen. 

### Normalisierungen

Normalisierungen bei: Datumsangabe, Geldbetrag

#### Datumsangabe 

Datumsangaben werden mit Herleitung normalisiert:

```
1422-08-21 / Freitag vor Bartholomäus (Mo 24.8.)ⒹActum an Freitag vor Bartholomei Anno domini Mº ccccº xxiiº
```

#### Geldbetrag

```
24 tl.Ⓟumb vier und zwainczig phunt Wienner phenning
1500 tl.Ⓟumb funfczehen hundert phunt phenning 
350 tl.Ⓟumb virdhalb hundert phunt phenning 
```

### kontrolliertes Vokabular

Kontrolliertes Vokabular bei: Lage, Ereignistyp

#### Lage

```
vor WidmertorⓁgelegen vor Widmertor ze Wienn
vordere PeckenstraßeⓁgelegen in der vodern Pekchenstrazz 
```

Wenn zusätzliche Information bekannt ist, kann sie ebenfalls eingetragen werden:

```
Lichtensteg, unter den FleischbänkenⓁganczes gelegen undern fleischpenkchen 
```

#### Ereignistyp

```
verkaufⒺhat verkaufft
kaufⒺmit kauf an In komen ist 
```

Die Label `Kauf` und `Verkauf` sollen möglichst nahe am Originaltext bleiben. Aus der Sicht einer Ontologie wie CIDOC CRM ist beides natürlich dasselbe: Es geht um ein Objekt O, Person X verkauft es an Person Y, bzw. Y kauft es von X, für einen Geldbetrag, mit Datum und Eintragungsgebühr. Diese zusätzliche Normalisierung übernimmt ein Skript. 

### IDs

IDs bei: Häusern (Objekt, Nachbarhaus) und Personen (von, an, evtl. Nachbarhaus)

Namensschema: 
* Objekte: D (für Ding), B (für Berlin), fortlaufende Nummerierung
* Personen: P (für Person), B (für Berlin), fortlaufende Nummerierung

#### Häuser

```
PBxxxxⓋAgnes von Lincz
verkaufⒺhat verkaufft

DB0001Ⓞain haus
vor WidmertorⓁgelegen vor Widmertor ze Wienn
DB0002, PBxxxxⓃzenegst Jacobin der Paugkerin haus
```

#### Personen

Personen können in Ⓥ, Ⓐ und indirekt in Ⓝ vorkommen. Bisher analysieren wir diese Slots nicht weiter. Stattdessen haben wir begonnen, sondern eine Liste von Personen (bzw. von Personennennungen) zu führen.

Ein Beispiel:

```
ⓋLinhart und Thoman gebruder die Taler bey Ryed gesessen 
und Dyemut Ir Swester Hainreich des Nuendorffer auch bey Ryed hausfraw 
alle drew Cristans aus dem Tal seligen kinder
```

```
P0001 Linhart Taler, wohnt bei Ried, Sohn von P0005
P0002 Thoman Taler, Bruder von P0001, wohnt bei Ried, Sohn von P0005
P0003 Dyemut, Ehefrau von P0004, Tochter von P0005
P0004 Hainreich der Nuendorffer, wohnt bei Ried
P0005 Cristan aus dem Tal (zum Zeitpunkt des Eintrags tot)
```

Wenn man nach einer dieser Personen sucht, wird die gesamte Textstelle als ein Suchtreffer angezeigt. 


## Weitere Themen

### Anfang und Ende eines Slots

Normalerweise entspricht eine Zeile einem Slot. Bestimmte Slots wie Ⓥ können zur besseren Lesbarkeit auch über mehrere Zeilen gehen. Bei einer Leerzeile ist ein Slot definitiv zuende. 

TODO: Falls genauere Markierungen nötig werden, können wir eine Schreibweise wie 

```
Ⓐdem erbern mann #Veiten dem Valkchner#
und frawn #Barbaren seiner hausfrawn#
```

ergänzen. Mit oder ohne TEI haben wir noch keine richtige Idee, wie ich das hier markieren würden:

```
ⓋLinhart und Thoman gebruder die Taler bey Ryed gesessen 
und Dyemut Ir Swester Hainreich des Nuendorffer auch bey Ryed hausfraw 
alle drew Cristans aus dem Tal seligen kinder
```

### Einträge mit mehreren Ereignissen

Das `an` in einem Ereignis entspricht normalerweise dem `von` im nächsten Ereignis. 

Insbesondere die Markierung der Ereignisse ist auch bei mir noch experimentell. Aber allgemein habe ich bei einem Eintrag einen Anfangszustand (d.h. wem das Haus gehört) und ein oder mehrere Ereignisse, die jeweils einen neuen Zustand bewirken. Das kann ich so markieren und durchnummerieren. Für unsere Daten ist es sinnvoll, nicht die Reihenfolge im Text, sondern die logische Reihenfolge zu verwenden (oft ist das auch das gleiche). Wenn also ein komplexer Eintrag mit drei Ereignissen anfängt mit

Hainreich Stumphwegk der sneider und Anna sein hausfraw 
habent emphangen nucz und gewer 

dann wäre das LⒶ, also das "an" des letzten Ereignisses.

Es müssen nicht alle Zustände und Ereignisse explizit dastehen. Zum Beispiel kann dastehen "das Haus, das vorher X und seiner Frau Y gehört hat" oder "das X und seine Frau Y gekauft hatten". Beides bedeutet, dass der Eintrag davor hoffentlich geendet hat mit dem Zustand "X und Y besitzen das Haus". Aber auch die Schreiber wollten ja, dass man die Einträge später noch versteht. 

Zum Beispiel die Hauspreise kann ich jederzeit mit einem Skript aus dem Text in eine Tabelle kopieren. Aber die Daten leben in der Formularansicht, nicht in einer Datenbank. Korrekturen würde ich in der Formularansicht machen und die entsprechende Tabelle dann auf Knopfdruck aktualisieren. Mit Ereignissen werde ich es ähnlich wie mit Preisen machen, aber Ereignisse sind komplexer und zurzeit sitzt auch eine SHK daran, Ereignisse herauszuziehen. Und die Daten sind immer nur so gut, wie sie im Text markiert wurden, aber das ist bei einer von Hand erstellten Excel-Tabelle ja nicht anders. 


