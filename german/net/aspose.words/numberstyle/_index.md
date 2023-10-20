---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words für .NET
description: Aspose.Words.NumberStyle opsomming. Gibt den Nummernstil für eine Liste Fußnoten und Endnoten sowie Seitenzahlen an in C#.
type: docs
weight: 4310
url: /de/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Gibt den Nummernstil für eine Liste, Fußnoten und Endnoten sowie Seitenzahlen an.

```csharp
public enum NumberStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Arabic | `0` | Arabische Nummerierung (1, 2, 3, ...) |
| UppercaseRoman | `1` | Großbuchstaben Roman (I, II, III, ...) |
| LowercaseRoman | `2` | Kleinbuchstaben römisch (i, ii, iii, ...) |
| UppercaseLetter | `3` | Großbuchstabe (A, B, C, ...) |
| LowercaseLetter | `4` | Kleinbuchstabe (a, b, c, ...) |
| Ordinal | `5` | Ordinalzahl (1., 2., 3., ...) |
| Number | `6` | Nummeriert (Eins, Zwei, Drei, ...) |
| OrdinalText | `7` | Ordinalzahl (Text) (Erster, Zweiter, Dritter, ...) |
| Hex | `8` | Hexadezimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicago Manual of Style: *, †, † |
| Kanji | `10` | Ideograph-digital |
| KanjiDigit | `11` | Japanisches Zählen |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Arabisch in voller Breite: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Halbbreites Arabisch: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japanisch legal |
| KanjiTraditional2 | `17` | Japanischer digitaler Zehntausender |
| NumberInCircle | `18` | Eingeschlossene Kreise |
| DecimalFullWidth | `19` | Dezimale volle Breite: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo volle Breite |
| Iroha | `21` | Iroha volle Breite |
| LeadingZero | `22` | Führende Null (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Aufzählungszeichen (überprüfen Sie den Zeichencode im Text) |
| Ganada | `24` | Koreanisches Ganada |
| Chosung | `25` | Korea Chosung |
| GB1 | `26` | Geschlossener Punkt |
| GB2 | `27` | Eingeschlossene Klammer |
| GB3 | `28` | Eingeschlossener Kreis Chinese |
| GB4 | `29` | Ideogramm eingeschlossener Kreis |
| Zodiac1 | `30` | Ideogramm Traditional |
| Zodiac2 | `31` | Ideogramm Zodiac |
| Zodiac3 | `32` | Ideogramm Sternzeichen Traditional |
| TradChinNum1 | `33` | Taiwanesisches Zählen |
| TradChinNum2 | `34` | Ideogramm legal Traditional |
| TradChinNum3 | `35` | Taiwaner zählen tausend |
| TradChinNum4 | `36` | Taiwanesisch digital |
| SimpChinNum1 | `37` | Chinesisches Zählen |
| SimpChinNum2 | `38` | Vereinfachtes chinesisches Recht |
| SimpChinNum3 | `39` | Chinesisch Tausend zählen |
| SimpChinNum4 | `40` | Chinesisch (nicht implementiert) |
| HanjaRead | `41` | Koreanisch digital |
| HanjaReadDigit | `42` | Koreanisches Zählen |
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
| ThaiCardinalText | `55` | Thailändische Beschreibung (Kardinäle) |
| VietCardinalText | `56` | Vietnamesische Beschreibung (Kardinäle) |
| NumberInDash | `57` | Seitenzahlenformat: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Russisches Kleinbuchstabenalphabet |
| UppercaseRussian | `59` | Russisches Großbuchstabenalphabet |
| None | `255` | Kein Aufzählungszeichen oder keine Nummer. |
| Custom | `65280` | Benutzerdefiniertes Zahlenformat. Es wird nur vom DOCX-Format unterstützt. |

## Beispiele

Zeigt, wie Sie bei Verwendung von DocumentBuilder eine benutzerdefinierte Listenformatierung auf Absätze anwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
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
