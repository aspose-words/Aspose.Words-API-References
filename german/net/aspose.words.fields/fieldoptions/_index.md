---
title: FieldOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert Optionen zur Steuerung der Feldbehandlung in einem Dokument.
type: docs
weight: 2100
url: /de/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Repräsentiert Optionen zur Steuerung der Feldbehandlung in einem Dokument.

```csharp
public sealed class FieldOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Ruft benutzerdefinierten Barcode-Generator ab oder legt ihn fest. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Ruft Pfade von in MS Word integrierten Vorlagen ab oder legt sie fest. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Ruft den Evaluator für Feldvergleichsausdrücke ab oder legt ihn fest. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Ruft die aktuellen Benutzerinformationen ab oder legt sie fest. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Ruft benutzerdefiniertes Trennzeichen für den \t-Schalter ab oder legt es fest[`FieldToc`](../fieldtoc/) Feld. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Ruft den Namen des Autors des Standarddokuments ab oder legt ihn fest. Wenn der Name des Autors bereits in den integrierten Dokumenteigenschaften angegeben ist, wird diese Option nicht berücksichtigt. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Ruft einen Anbieter ab oder legt ihn fest, der ein Abfrageergebnis für zurückgibt[`FieldDatabase`](../fielddatabase/) Feld. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Holt oder setzt a[`FieldIndexFormat`](./fieldindexformat/) das repräsentiert die Formatierung für die[`FieldIndex`](../fieldindex/)Felder im Dokument. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Ruft einen Anbieter ab oder legt einen Anbieter fest, der ein Kulturobjekt zurückgibt, das für jedes bestimmte Feld spezifisch ist. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Gibt an, welche Kultur verwendet werden soll, um das Feldergebnis zu formatieren. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Holt oder setzt[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementierung |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Ruft den Dateinamen des Dokuments ab oder setzt ihn. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, ob das Legacy-Zahlenformat (vor AW 13.10) für Felder aktiviert ist oder nicht. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Ruft die Kultur ab oder legt sie fest, um Feldwerte vorzuverarbeiten. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Ermöglicht die Steuerung der Formatierung des Feldergebnisses. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt ihn fest. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Ruft die Kategorien der Normtabelle ab oder legt sie fest. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der angibt, dass das Zahlenformat mit invarianter Kultur oder not geparst wird |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Ruft Benutzereingabeaufforderungen während der Feldaktualisierung ab oder legt sie fest. |

### Beispiele

Zeigt, wie die Quelle der Kultur angegeben wird, die für die Datumsformatierung während einer Feldaktualisierung oder eines Seriendrucks verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Briefvorlagenfelder mit deutschem Gebietsschema einfügen.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Setzt die aktuelle Kultur auf US-Englisch, nachdem der ursprüngliche Wert in einer Variablen beibehalten wurde.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Diese Zusammenführung verwendet die Kultur des aktuellen Threads, um das Datum zu formatieren, US-Englisch.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurieren Sie die nächste Zusammenführung, um ihren Kulturwert aus dem Feldcode zu beziehen. Der Wert dieser Kultur wird deutsch sein.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Das erste Merge-Ergebnis enthält ein englisch formatiertes Datum, das zweite ein deutsch formatiertes Datum.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Stellen Sie die ursprüngliche Kultur des Threads wieder her.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
