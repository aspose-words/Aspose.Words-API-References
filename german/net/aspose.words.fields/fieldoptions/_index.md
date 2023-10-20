---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.FieldOptions klas. Stellt Optionen zur Steuerung der Feldverarbeitung in einem Dokument dar in C#.
type: docs
weight: 2250
url: /de/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Stellt Optionen zur Steuerung der Feldverarbeitung in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public sealed class FieldOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Ruft den benutzerdefinierten Barcode-Generator ab oder legt ihn fest. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Ruft einen Anbieter ab oder legt ihn fest, der einen Bibliografiestil für zurückgibt[`FieldBibliography`](../fieldbibliography/) Und[`FieldCitation`](../fieldcitation/) Felder. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Ruft Pfade der in MS Word integrierten Vorlagen ab oder legt diese fest. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Ruft den Feldvergleichsausdruck-Evaluator ab oder legt ihn fest. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Ruft die aktuellen Benutzerinformationen ab oder legt diese fest. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Ruft ein benutzerdefiniertes Stiltrennzeichen für den \t-Schalter ab oder legt es fest[`FieldToc`](../fieldtoc/) field. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Ruft den Standardnamen des Dokumentautors ab oder legt diesen fest. Wenn der Name des Autors bereits in den integrierten Dokumenteigenschaften angegeben ist, wird diese Option nicht berücksichtigt. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Ruft einen Anbieter ab oder legt diesen fest, der ein Abfrageergebnis für zurückgibt[`FieldDatabase`](../fielddatabase/) field. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Ruft a ab oder legt es fest[`FieldIndexFormat`](./fieldindexformat/) das repräsentiert die Formatierung für die[`FieldIndex`](../fieldindex/) Felder im Dokument. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Ruft einen Anbieter ab oder legt diesen fest, der ein für jedes bestimmte Feld spezifisches Kulturobjekt zurückgibt. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Gibt an, welche Kultur zum Formatieren des Feldergebnisses verwendet werden soll. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Ruft ab oder legt fest[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) Implementierung |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Ruft ab oder legt fest[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) Implementierung. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Ruft den Dateinamen des Dokuments ab oder legt ihn fest. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Ruft den Wert ab oder legt diesen fest, der angibt, ob das alte Zahlenformat (früher als AW 13.10) für Felder aktiviert ist oder nicht. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Ruft die Kultur ab oder legt sie fest, um Feldwerte vorzuverarbeiten. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Ermöglicht die Steuerung der Formatierung des Feldergebnisses. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt diesen fest. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Ruft die Tabelle der Autoritätskategorien ab oder legt diese fest. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, dass das Zahlenformat mithilfe der invarianten Kultur analysiert wird oder nicht |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Ruft den Befragten während der Feldaktualisierung ab oder legt ihn auf Benutzeraufforderungen fest. |

## Beispiele

Zeigt, wie Sie die Quelle der Kultur angeben, die für die Datumsformatierung während einer Feldaktualisierung oder eines Seriendrucks verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Zusammenführungsfelder mit deutschem Gebietsschema einfügen.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Setze die aktuelle Kultur auf US-Englisch, nachdem der ursprüngliche Wert in einer Variablen beibehalten wurde.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bei dieser Zusammenführung wird die Kultur des aktuellen Threads verwendet, um das Datum zu formatieren, US-Englisch.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurieren Sie die nächste Zusammenführung so, dass ihr Kulturwert aus dem Feldcode stammt. Der Wert dieser Kultur wird deutsch sein.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Das erste Zusammenführungsergebnis enthält ein in Englisch formatiertes Datum, während das zweite in Deutsch formatiert ist.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Die ursprüngliche Kultur des Threads wiederherstellen.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
