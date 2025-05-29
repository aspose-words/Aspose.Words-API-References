---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldOptions för att optimera fälthanteringen i dokument, vilket förbättrar ditt arbetsflöde och effektiviserar dokumenthanteringen.
type: docs
weight: 2660
url: /sv/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Representerar alternativ för att styra fälthantering i ett dokument.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public sealed class FieldOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Hämtar eller ställer in en anpassad streckkodsgenerator. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Hämtar eller ställer in en leverantör som returnerar en bibliografistil för [`FieldBibliography`](../fieldbibliography/) och[`FieldCitation`](../fieldcitation/) fält. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Hämtar eller anger sökvägar för inbyggda mallar i MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Hämtar eller ställer in utvärderaren för fältjämförelseuttryck. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Hämtar eller ställer in aktuell användarinformation. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Hämtar eller ställer in anpassad stilavgränsare för \t-växeln i[`FieldToc`](../fieldtoc/) fält. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Hämtar eller anger standardnamnet på dokumentförfattaren. Om författarnamnet redan är angett i de inbyggda dokumentegenskaperna, beaktas inte det här alternativet. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Hämtar eller ställer in en provider som returnerar ett frågeresultat för[`FieldDatabase`](../fielddatabase/) fält. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Hämtar eller ställer in en[`FieldIndexFormat`](./fieldindexformat/) som representerar formateringen för[`FieldIndex`](../fieldindex/) fält i dokumentet. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Hämtar eller ställer in en provider som returnerar ett kulturobjekt som är specifikt för varje enskilt fält. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Anger vilken kultur som ska användas för att formatera fältresultatet. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Hämtar eller sätter[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementering |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Hämtar eller sätter[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) implementering. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Hämtar eller anger dokumentets filnamn. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Hämtar eller ställer in värdet som anger om dubbelriktad text stöds fullt ut under fältuppdatering eller inte. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Hämtar eller ställer in värdet som anger om äldre (tidigare än AW 13.10) talformat för fält är aktiverat eller inte. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Hämtar eller ställer in kulturen att förbehandla fältvärden. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Gör det möjligt att styra hur fältresultatet formateras. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Hämtar eller anger filnamnet på mallen som används av dokumentet. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Hämtar eller ställer in tabellen över auktoritetskategorier. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Hämtar eller ställer in värdet som anger att talformatet analyseras med hjälp av invariant kultur eller inte |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Hämtar eller ställer in respondenten på användarfrågor under fältuppdatering. |

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
