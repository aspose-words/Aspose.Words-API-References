---
title: GeneralFormatCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GeneralFormatCollection Count för att enkelt komma åt det totala antalet objekt i din samling, vilket förbättrar effektiviteten i datahanteringen.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/generalformatcollection/count/
---
## GeneralFormatCollection.Count property

Hämtar det totala antalet objekt i samlingen.

```csharp
public int Count { get; }
```

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

* class [GeneralFormatCollection](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
