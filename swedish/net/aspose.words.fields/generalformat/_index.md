---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Fields.GeneralFormat, som förbättrar numerisk textformatering för fält, vilket säkerställer tydlighet och precision i dina dokument.
type: docs
weight: 3050
url: /sv/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Anger ett generellt format som tillämpas på ett numeriskt, text- eller fältresultat. Ett fält kan ha en kombination av allmänna format.

```csharp
public enum GeneralFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Används för att ange ett saknat generellt format. |
| Aiueo | `1` | Numerisk formatering. Formaterar ett numeriskt resultat med hiragana-tecken i traditionell aiueo-ordning. |
| UppercaseAlphabetic | `2` | Numerisk formatering. Formaterar ett numeriskt resultat som en eller flera förekomster av ett versalt latinskt tecken. |
| LowercaseAlphabetic | `3` | Numerisk formatering. Formaterar ett numeriskt resultat som en eller flera förekomster av ett gement alfabetiskt latinskt tecken. |
| Arabic | `4` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av arabiska kardinalsiffror. |
| ArabicAbjad | `5` | Numerisk formatering. Formaterar ett numeriskt resultat med stigande Abjad-siffror. |
| ArabicAlpha | `6` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av tecken i det arabiska alfabetet. |
| ArabicDash | `7` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av arabiska kardinalsiffror, med prefixet "-" och suffixet "-". |
| BahtText | `8` | Numerisk formatering. Formaterar ett numeriskt resultat i det thailändska räknesystemet. |
| CardText | `9` | Numerisk formatering. Huvudtext (Ett, Två, Tre, ...). |
| ChineseNum1 | `10` | Numerisk formatering. Formaterar ett numeriskt resultat med stigande tal från lämpligt räknesystem. |
| ChineseNum2 | `11` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från lämpligt juridiskt format. |
| ChineseNum3 | `12` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från lämpligt tusentalsräknesystem. |
| Chosung | `13` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från det koreanska Chosung-formatet. |
| CircleNum | `14` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av decimalnumrering omgiven av en cirkel, med hjälp av det alfanumeriska tecknet omgivna för tal i intervallet 1–20. |
| DBChar | `15` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av dubbelbyte arabisk numrering. |
| DBNum1 | `16` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella digitala ideogram, med lämpligt tecken. |
| DBNum2 | `17` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från lämpligt räknesystem. |
| DBNum3 | `18` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från lämpligt juridiskt räknesystem. |
| DBNum4 | `19` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från lämpligt digitalt räknesystem. |
| DollarText | `20` | Numerisk formatering. Dollartext (Ett, Två, Tre, ... + OCH 55/100). |
| Ganada | `21` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från det koreanska Ganada-formatet. |
| GB1 | `22` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av decimalnummer följt av en punkt, med hjälp av det omslutna alfanumeriska tecknet. |
| GB2 | `23` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av decimalnumrering inom parentes, med hjälp av det omslutna alfanumeriska tecknet. |
| GB3 | `24` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av decimaltal omgivet av en cirkel, med hjälp av det alfanumeriska tecknet omgivet. |
| GB4 | `25` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av decimaltal omgivet av en cirkel, med hjälp av det alfanumeriska tecknet omgivet. |
| Hebrew1 | `26` | Numerisk formatering. Formaterar ett numeriskt resultat med hebreiska siffror. |
| Hebrew2 | `27` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av det hebreiska alfabetet. |
| Hex | `28` | Numerisk formatering. Formaterar det numeriska resultatet med hjälp av hexadecimala siffror i versaler. |
| HindiArabic | `29` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av hindi-tal. |
| HindiCardText | `30` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från det hindi-räknesystemet. |
| HindiLetter1 | `31` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av hindi-vokaler. |
| HindiLetter2 | `32` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av hindi-konsonanter. |
| Iroha | `33` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av japanska iroha. |
| KanjiNum1 | `34` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av en japansk stil och lämpligt räknesystem. |
| KanjiNum2 | `35` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av lämpligt räknesystem. |
| KanjiNum3 | `36` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av lämpligt räknesystem. |
| Ordinal | `37` | Numerisk formatering. Ordinal (1:a, 2:a, 3:e, ...). |
| OrdText | `38` | Numerisk formatering. Ordinär text (första, andra, tredje, ...). |
| UppercaseRoman | `39` | Numerisk formatering. Versaler i romerska bokstäver (I, II, III, ...). |
| LowercaseRoman | `40` | Numerisk formatering. Gemener romerska bokstäver (i, ii, iii, ...). |
| SBChar | `41` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av arabisk numrering i en byte. |
| ThaiArabic | `42` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av thailändska tal. |
| ThaiCardText | `43` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella tal från det thailändska räknesystemet. |
| ThaiLetter | `44` | Numerisk formatering. Formaterar ett numeriskt resultat med thailändska bokstäver. |
| VietCardText | `45` | Numerisk formatering. Formaterar ett numeriskt resultat med vietnamesiska siffror. |
| Zodiac1 | `46` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av traditionella sekventiella numeriska ideogram. |
| Zodiac2 | `47` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella zodiak-ideogram. |
| Zodiac3 | `48` | Numerisk formatering. Formaterar ett numeriskt resultat med hjälp av sekventiella traditionella zodiakideogram. |
| Caps | `49` | Textformatering. Skriver första bokstaven i varje ord som versal. |
| FirstCap | `50` | Textformatering. Skriver den första bokstaven i det första ordet till stor bokstav. |
| Lower | `51` | Textformatering. Alla bokstäver är gemener. |
| Upper | `52` | Textformatering. Alla bokstäver är versaler. |
| CharFormat | `53` | Formatering av fältresultat. CHARFORMAT-instruktionen. |
| MergeFormat | `54` | Formatering av fältresultat. MERGEFORMAT-instruktionen. |
| MergeFormatInet | `55` | Formatering av fältresultat. MERGEFORMATINET-instruktionen. |

## Exempel

Visar hur man formaterar fältresultat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en dokumentbyggare för att infoga ett fält som visar ett resultat utan formatering.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Vi kan tillämpa ett format på ett fälts resultat med hjälp av fältets egenskaper.
// Nedan följer tre typer av format som vi kan tillämpa på ett fälts resultat.
// 1 - Numeriskt format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Datum-/tidsformat:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Allmänt format:
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

// Vi kan ta bort våra format för att återställa fältets resultat till dess ursprungliga form.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
