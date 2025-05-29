---
title: FieldUpdateCultureSource Enum
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fields.FieldUpdateCultureSource. Kontrollera fältuppdateringar med anpassningsbara kulturinställningar för förbättrad dokumentnoggrannhet.
type: docs
weight: 2970
url: /sv/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

Anger vilken kultur som ska användas under fältuppdatering.

```csharp
public enum FieldUpdateCultureSource
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| CurrentThread | `0` | Kulturen för den aktuella exekveringstråden används för att uppdatera fält. |
| FieldCode | `1` | Den kultur som anges i fältets formateringsegenskaper via språkinställningen används. |

## Exempel

Visar hur man anger källan för den kultur som används för datumformatering under en fältuppdatering eller dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två mergefält med tysk språkinställning.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Ställ in den aktuella kulturen till amerikansk engelska efter att ha bevarat dess ursprungliga värde i en variabel.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Denna sammanslagning kommer att använda den aktuella trådens kultur för att formatera datumet, amerikansk engelska.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurera nästa sammanslagning så att dess kulturvärde hämtas från fältkoden. Värdet för den kulturen kommer att vara tyskt.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Det första sammanslagningsresultatet innehåller ett datum formaterat på engelska, medan det andra är på tyska.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Återställ trådens ursprungliga kultur.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
