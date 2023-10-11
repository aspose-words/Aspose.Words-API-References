---
title: Class GeneralFormatCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.GeneralFormatCollection klass. Representerar en maskinskriven samling allmänna format.
type: docs
weight: 2650
url: /sv/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Representerar en maskinskriven samling allmänna format.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Får det totala antalet föremål i samlingen. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Får ett allmänt format vid angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(GeneralFormat) | Lägger till ett allmänt format till samlingen. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(GeneralFormat) | Tar bort alla förekomster av det angivna allmänna formatet från samlingen. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(int) | Tar bort en allmän formatförekomst vid det angivna indexet. |

### Exempel

Visar hur man formaterar fältresultat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en dokumentbyggare för att infoga ett fält som visar ett resultat utan format.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Vi kan tillämpa ett format på ett fälts resultat med hjälp av fältets egenskaper.
// Nedan finns tre typer av format som vi kan tillämpa på ett fälts resultat.
// 1 - Numeriskt format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Datum/tid format:
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

* enum [GeneralFormat](../generalformat/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


