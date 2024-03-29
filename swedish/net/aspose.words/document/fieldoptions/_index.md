---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words för .NET
description: Document FieldOptions fast egendom. Får enFieldOptions objekt som representerar alternativ för att styra fälthanteringen i dokumentet i C#.
type: docs
weight: 120
url: /sv/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Får en[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) objekt som representerar alternativ för att styra fälthanteringen i dokumentet.

```csharp
public FieldOptions FieldOptions { get; }
```

## Exempel

Visar hur man anger källan till kulturen som används för datumformatering under en fältuppdatering eller e-postsammanfogning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två sammanslagningsfält med tysk språk.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Ställ in den nuvarande kulturen till amerikansk engelska efter att ha bevarat dess ursprungliga värde i en variabel.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Denna sammanslagning kommer att använda den aktuella trådens kultur för att formatera datumet, amerikansk engelska.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurera nästa sammanslagning för att hämta dess kulturvärde från fältkoden. Värdet av den kulturen kommer att vara tysk.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Det första sammanslagningsresultatet innehåller ett datum formaterat på engelska, medan det andra är på tyska.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Återställ trådens ursprungliga kultur.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Se även

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
