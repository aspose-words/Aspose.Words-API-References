---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldOptions, um die Feldverarbeitung in Dokumenten zu optimieren und so Ihren Arbeitsablauf und die Effizienz Ihres Dokumentenmanagements zu verbessern.
type: docs
weight: 2660
url: /de/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Stellt Optionen zur Steuerung der Feldbehandlung in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public sealed class FieldOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Ruft einen benutzerdefinierten Barcode-Generator ab oder legt ihn fest. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Ruft einen Provider ab oder legt ihn fest, der einen Bibliographiestil für zurückgibt.[`FieldBibliography`](../fieldbibliography/) Und[`FieldCitation`](../fieldcitation/) Felder. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Ruft die Pfade der in MS Word integrierten Vorlagen ab oder legt sie fest. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Ruft den Evaluator für Feldvergleichsausdrücke ab oder legt ihn fest. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Ruft die aktuellen Benutzerinformationen ab oder legt sie fest. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Ruft einen benutzerdefinierten Stiltrenner für den \t-Schalter ab oder legt ihn fest in[`FieldToc`](../fieldtoc/) Feld. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Ruft den Standardnamen des Dokumentautors ab oder legt ihn fest. Wenn der Name des Autors bereits in den integrierten Dokumenteigenschaften angegeben ist, wird diese Option nicht berücksichtigt. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Ruft einen Provider ab oder legt ihn fest, der ein Abfrageergebnis für die[`FieldDatabase`](../fielddatabase/) Feld. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Ruft ab oder setzt einen[`FieldIndexFormat`](./fieldindexformat/) das stellt die Formatierung für die[`FieldIndex`](../fieldindex/) Felder im Dokument. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Ruft einen Anbieter ab oder legt ihn fest, der ein für jedes einzelne Feld spezifisches Kulturobjekt zurückgibt. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Gibt an, welche Kultur zum Formatieren des Feldergebnisses verwendet werden soll. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Ruft ab oder legt fest[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) Implementierung |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Ruft ab oder legt fest[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) Implementierung. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Ruft den Dateinamen des Dokuments ab oder legt ihn fest. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, ob das veraltete Zahlenformat (vor AW 13.10) für Felder aktiviert ist oder nicht. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Ruft die Kultur zur Vorverarbeitung von Feldwerten ab oder legt sie fest. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Ermöglicht die Steuerung der Formatierung des Feldergebnisses. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt ihn fest. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Ruft die Kategorien des Rechtsgrundlagenverzeichnisses ab oder legt sie fest. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, ob das Zahlenformat mit invarianter Kultur analysiert wird oder nicht |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Ruft den Befragten für Benutzeraufforderungen während der Feldaktualisierung ab oder legt ihn fest. |

## Beispiele

Zeigt, wie die Quelle der Kultur angegeben wird, die während einer Feldaktualisierung oder eines Seriendrucks für die Datumsformatierung verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Seriendruckfelder mit deutscher Gebietseinstellung einfügen.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Stellen Sie die aktuelle Kultur auf US-Englisch ein, nachdem Sie den ursprünglichen Wert in einer Variablen beibehalten haben.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bei dieser Zusammenführung wird die Kultur des aktuellen Threads (US-Englisch) zum Formatieren des Datums verwendet.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurieren Sie die nächste Zusammenführung so, dass der Kulturwert aus dem Feldcode stammt. Der Wert dieser Kultur ist Deutsch.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Das erste Zusammenführungsergebnis enthält ein Datum im englischen Format, während das zweite im deutschen Format ist.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Die ursprüngliche Kultur des Threads wiederherstellen.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
