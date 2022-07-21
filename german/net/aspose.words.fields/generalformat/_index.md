---
title: GeneralFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt ein allgemeines Format an das auf ein numerisches Text- oder beliebiges Feldergebnis angewendet wird. Ein Feld kann eine Kombination aus allgemeinen Formaten aufweisen.
type: docs
weight: 2480
url: /de/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Gibt ein allgemeines Format an, das auf ein numerisches, Text- oder beliebiges Feldergebnis angewendet wird. Ein Feld kann eine Kombination aus allgemeinen Formaten aufweisen.

```csharp
public enum GeneralFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Wird verwendet, um ein fehlendes allgemeines Format anzugeben. |
| Aiueo | `1` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hiragana-Zeichen in der traditionellen aiueo-Reihenfolge. |
| UppercaseAlphabetic | `2` | Numerische Formatierung. Formatiert ein numerisches Ergebnis als ein oder mehrere Vorkommen eines lateinischen Großbuchstabens. |
| LowercaseAlphabetic | `3` | Numerische Formatierung. Formatiert ein numerisches Ergebnis als ein oder mehrere Vorkommen eines lateinischen Kleinbuchstabens. |
| Arabic | `4` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit arabischen Kardinalzahlen. |
| ArabicAbjad | `5` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit aufsteigenden Abjad-Ziffern. |
| ArabicAlpha | `6` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Zeichen des arabischen Alphabets. |
| ArabicDash | `7` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit arabischen Kardinalzahlen mit dem Präfix „-“ und dem Suffix „-“. |
| BahtText | `8` | Numerische Formatierung. Formatiert ein numerisches Ergebnis im thailändischen Zählsystem. |
| CardText | `9` | Numerische Formatierung. Kardinaltext (Eins, Zwei, Drei, ...). |
| ChineseNum1 | `10` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit aufsteigenden Zahlen aus dem entsprechenden Zählsystem. |
| ChineseNum2 | `11` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden gesetzlichen Format. |
| ChineseNum3 | `12` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden Tausendersystem. |
| Chosung | `13` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem koreanischen Chosung-Format. |
| CircleNum | `14` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit einer in einen Kreis eingeschlossenen Dezimalzahl und verwendet das eingeschlossene alphanumerische Glyphenzeichen für Zahlen im Bereich 1–20. |
| DBChar | `15` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit arabischer Doppelbyte-Nummerierung. |
| DBNum1 | `16` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit sequentiellen digitalen Ideogrammen unter Verwendung des entsprechenden Zeichens. |
| DBNum2 | `17` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden Zählsystem. |
| DBNum3 | `18` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden gesetzlichen Zählsystem. |
| DBNum4 | `19` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden digitalen Zählsystem. |
| DollarText | `20` | Numerische Formatierung. Dollartext (Eins, Zwei, Drei, ... + UND 55/100). |
| Ganada | `21` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem koreanischen Ganada-Format. |
| GB1 | `22` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit einer Dezimalzahl, gefolgt von einem Punkt, und verwendet das eingeschlossene alphanumerische Glyphenzeichen. |
| GB2 | `23` | Numerische Formatierung. Formatiert ein numerisches Ergebnis unter Verwendung der in Klammern eingeschlossenen Dezimalzahl unter Verwendung des eingeschlossenen alphanumerischen Glyphenzeichens. |
| GB3 | `24` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit einer in einen Kreis eingeschlossenen Dezimalnummerierung unter Verwendung des eingeschlossenen alphanumerischen Glyphenzeichens . |
| GB4 | `25` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit einer in einen Kreis eingeschlossenen Dezimalnummerierung unter Verwendung des eingeschlossenen alphanumerischen Glyphenzeichens . |
| Hebrew1 | `26` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit hebräischen Ziffern. |
| Hebrew2 | `27` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem hebräischen Alphabet. |
| Hex | `28` | Numerische Formatierung. Formatiert das numerische Ergebnis mit Hexadezimalziffern in Großbuchstaben. |
| HindiArabic | `29` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hindi-Zahlen. |
| HindiCardText | `30` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem Hindi-Zählsystem. |
| HindiLetter1 | `31` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hindi-Vokalen. |
| HindiLetter2 | `32` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hindi-Konsonanten. |
| Iroha | `33` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem japanischen iroha. |
| KanjiNum1 | `34` | Numerische Formatierung. Formatiert ein numerisches Ergebnis im japanischen Stil mit dem entsprechenden Zählsystem. |
| KanjiNum2 | `35` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem entsprechenden Zählsystem. |
| KanjiNum3 | `36` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem entsprechenden Zählsystem. |
| Ordinal | `37` | Numerische Formatierung. Ordnungszahl (1., 2., 3., ...). |
| OrdText | `38` | Numerische Formatierung. Ordnungstext (Erster, Zweiter, Dritter, ...). |
| UppercaseRoman | `39` | Numerische Formatierung. Großbuchstaben Roman (I, II, III, ...). |
| LowercaseRoman | `40` | Numerische Formatierung. Kleinbuchstaben Roman (i, ii, iii, ...). |
| SBChar | `41` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit arabischer Einzelbyte-Nummerierung. |
| ThaiArabic | `42` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit thailändischen Zahlen. |
| ThaiCardText | `43` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem thailändischen Zählsystem. |
| ThaiLetter | `44` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit thailändischen Buchstaben. |
| VietCardText | `45` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit vietnamesischen Ziffern. |
| Zodiac1 | `46` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden numerischen traditionellen Ideogrammen. |
| Zodiac2 | `47` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit sequentiellen Tierkreiszeichen. |
| Zodiac3 | `48` | Numerische Formatierung. Formatiert ein numerisches Ergebnis mit sequenziellen traditionellen Tierkreis-Ideogrammen. |
| Caps | `49` | Textformatierung. Schreibt den ersten Buchstaben jedes Wortes groß. |
| FirstCap | `50` | Textformatierung. Schreibt den ersten Buchstaben des ersten Wortes groß. |
| Lower | `51` | Textformatierung. Alle Buchstaben sind Kleinbuchstaben. |
| Upper | `52` | Textformatierung. Alle Buchstaben sind Großbuchstaben. |
| CharFormat | `53` | Feldergebnisformatierung. Die Anweisung CHARFORMAT. |
| MergeFormat | `54` | Feldergebnisformatierung. Die Anweisung MERGEFORMAT. |
| MergeFormatInet | `55` | Feldergebnisformatierung. Die Anweisung MERGEFORMATINET. |

### Beispiele

Zeigt, wie Feldergebnisse formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Dokumentenersteller, um ein Feld einzufügen, das ein Ergebnis ohne angewendetes Format anzeigt.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Wir können ein Format auf das Ergebnis eines Felds anwenden, indem wir die Eigenschaften des Felds verwenden.
// Nachfolgend sind drei Arten von Formaten aufgeführt, die wir auf das Ergebnis eines Felds anwenden können.
// 1 - Numerisches Format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Datums-/Uhrzeitformat:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Allgemeines Format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Wir können unsere Formate entfernen, um das Ergebnis des Felds auf seine ursprüngliche Form zurückzusetzen.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
