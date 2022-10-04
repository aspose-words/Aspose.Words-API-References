---
title: FieldOptions
second_title: Aspose.Words för .NET API Referens
description: Representerar alternativ för att styra fälthantering i ett dokument.
type: docs
weight: 2100
url: /sv/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Representerar alternativ för att styra fälthantering i ett dokument.

```csharp
public sealed class FieldOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Hämtar eller ställer in anpassad streckkodsgenerator. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Hämtar eller ställer in sökvägar för MS Words inbyggda mallar. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Hämtar eller ställer in utvärderaren för fältjämförelseuttryck. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Hämtar eller ställer in aktuell användarinformation. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Hämtar eller ställer in anpassad stilseparator för \t-växeln[`FieldToc`](../fieldtoc/) field. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Hämtar eller ställer in standarddokumentets författares namn. Om författarens namn redan är specificerat i inbyggda dokumentegenskaper, övervägs inte detta alternativ. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Hämtar eller ställer in en leverantör som returnerar ett frågeresultat för[`FieldDatabase`](../fielddatabase/) field. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Hämtar eller sätter en[`FieldIndexFormat`](./fieldindexformat/) som representerar formateringen för[`FieldIndex`](../fieldindex/)fält i dokumentet. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Hämtar eller ställer in en leverantör som returnerar ett kulturobjekt specifikt för varje särskilt fält. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Anger vilken kultur som ska användas för att formatera fältresultatet. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Hämtar eller sätter[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementering |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Hämtar eller ställer in filnamnet på dokumentet. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Hämtar eller ställer in värdet som anger om dubbelriktad text stöds fullt ut under fältuppdatering eller inte. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Hämtar eller ställer in värdet som anger om äldre (tidigt än AW 13.10) nummerformat för fält är aktiverat eller inte. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Hämtar eller ställer in kulturen för att förbehandla fältvärden. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Gör det möjligt att styra hur fältresultatet formateras. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Hämtar eller ställer in filnamnet på mallen som används av dokumentet. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Hämtar eller sätter tabellen över auktoritetskategorier. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Hämtar eller ställer in värdet som indikerar att talformatet tolkas med invariant kultur eller inte |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Hämtar eller ställer in svaranden till användarmeddelanden under fältuppdatering. |

### Exempel

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

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
