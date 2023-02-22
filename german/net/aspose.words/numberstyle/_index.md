---
title: Enum NumberStyle
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.NumberStyle opsomming. Gibt den Nummernstil für eine Liste Fußnoten und Endnoten Seitenzahlen an.
type: docs
weight: 4070
url: /de/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Gibt den Nummernstil für eine Liste, Fußnoten und Endnoten, Seitenzahlen an.

```csharp
public enum NumberStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Arabic | `0` | Arabische Nummerierung (1, 2, 3, ...) |
| UppercaseRoman | `1` | Großbuchstaben Roman (I, II, III, ...) |
| LowercaseRoman | `2` | Kleinbuchstaben Roman (i, ii, iii, ...) |
| UppercaseLetter | `3` | Großbuchstaben (A, B, C, ...) |
| LowercaseLetter | `4` | Kleinbuchstaben (a, b, c, ...) |
| Ordinal | `5` | Ordnungszahl (1., 2., 3., ...) |
| Number | `6` | Nummeriert (Eins, Zwei, Drei, ...) |
| OrdinalText | `7` | Ordnungszahl (Text) (Erster, Zweiter, Dritter, ...) |
| Hex | `8` | Hexadezimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicagoer Stilhandbuch: *, †, † |
| Kanji | `10` | Ideogramm-digital |
| KanjiDigit | `11` | Japanische Zählung |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Arabisch in voller Breite: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Halbbreite Arabisch: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japanisches Recht |
| KanjiTraditional2 | `17` | Japanische digitale Zehntausend |
| NumberInCircle | `18` | Eingeschlossene Kreise |
| DecimalFullWidth | `19` | Dezimalzahl volle Breite: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo volle Breite |
| Iroha | `21` | Iroha volle Breite |
| LeadingZero | `22` | Führende Null (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Aufzählungszeichen (überprüfen Sie den Zeichencode im Text) |
| Ganada | `24` | Koreanisches Ganada |
| Chosung | `25` | Korea Chosung |
| GB1 | `26` | Eingeschlossener Punkt |
| GB2 | `27` | Geschlossene Klammer |
| GB3 | `28` | Eingeschlossener Kreis Chinesisch |
| GB4 | `29` | Ideogramm geschlossener Kreis |
| Zodiac1 | `30` | Ideogramm traditionell |
| Zodiac2 | `31` | Ideogramm Sternzeichen |
| Zodiac3 | `32` | Ideogramm Sternzeichen traditionell |
| TradChinNum1 | `33` | Taiwanesische Zählung |
| TradChinNum2 | `34` | Ideogramm legal traditionell |
| TradChinNum3 | `35` | Taiwaner zählen tausend |
| TradChinNum4 | `36` | Taiwanesisch digital |
| SimpChinNum1 | `37` | Chinesische Zählung |
| SimpChinNum2 | `38` | Chinesisches Recht vereinfacht |
| SimpChinNum3 | `39` | Chinesische Zählung Tausend |
| SimpChinNum4 | `40` | Chinesisch (nicht implementiert) |
| HanjaRead | `41` | Koreanisch digital |
| HanjaReadDigit | `42` | Koreanische Zählung |
| Hangul | `43` | Korea legal |
| Hanja | `44` | Korea digital2 |
| Hebrew1 | `45` | Hebräisch-1 |
| Arabic1 | `46` | Arabisch alpha |
| Hebrew2 | `47` | Hebräisch-2 |
| Arabic2 | `48` | Arabisch abjad |
| HindiLetter1 | `49` | Hindi-Vokale |
| HindiLetter2 | `50` | Hindi-Konsonanten |
| HindiArabic | `51` | Hindi-Zahlen |
| HindiCardinalText | `52` | Hindi beschreibend (Kardinäle) |
| ThaiLetter | `53` | Thailändische Buchstaben |
| ThaiArabic | `54` | Thailändische Zahlen |
| ThaiCardinalText | `55` | Thailändisch beschreibend (Kardinäle) |
| VietCardinalText | `56` | vietnamesische Beschreibung (Kardinäle) |
| NumberInDash | `57` | Seitenzahlenformat: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Russisches Alphabet in Kleinbuchstaben |
| UppercaseRussian | `59` | Russisches Alphabet in Großbuchstaben |
| None | `255` | Kein Aufzählungszeichen oder Nummer. |
| Custom | `65280` | Benutzerdefiniertes Zahlenformat. Es wird nur vom DOCX-Format unterstützt. |

### Beispiele

Zeigt, wie Sie benutzerdefinierte Listenformatierungen auf Absätze anwenden, wenn Sie DocumentBuilder verwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft Word-Vorlage und passen Sie die ersten beiden Listenebenen an.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Dieser NumberFormat-Wert erstellt sternförmige Aufzählungssymbole.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Absätze erstellen und beide Listenebenen unserer benutzerdefinierten Listenformatierung darauf anwenden.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


