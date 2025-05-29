---
title: FieldFormat Class
linktitle: FieldFormat
articleTitle: FieldFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldFormat för enkel åtkomst till numeriska fält, datum- och tidsfält. Förbättra dokumentformateringen med kraftfulla funktioner!
type: docs
weight: 2350
url: /sv/net/aspose.words.fields/fieldformat/
---
## FieldFormat class

Ger åtkomst till fältens numeriska formatering, datum och tid samt allmän formatering med maskinskriven funktion.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DateTimeFormat](../../aspose.words.fields/fieldformat/datetimeformat/) { get; set; } | Hämtar eller ställer in en formatering som tillämpas på ett datum- och tidsfältresultat. Motsvarar växeln \@. |
| [GeneralFormats](../../aspose.words.fields/fieldformat/generalformats/) { get; } | Hämtar en samling allmänna format som tillämpas på ett numeriskt, text- eller valfritt fältresultat. Motsvarar \*-växlarna. |
| [NumericFormat](../../aspose.words.fields/fieldformat/numericformat/) { get; set; } | Hämtar eller ställer in en formatering som tillämpas på ett numeriskt fältresultat. Motsvarar växeln \#. |

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
