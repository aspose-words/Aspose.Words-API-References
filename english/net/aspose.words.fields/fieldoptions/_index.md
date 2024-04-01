---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldOptions class. Represents options to control field handling in a document in C#.
type: docs
weight: 2390
url: /net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Represents options to control field handling in a document.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public sealed class FieldOptions
```

## Properties

| Name | Description |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Gets or set custom barcode generator. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Gets or sets a provider that returns a bibliography style for the [`FieldBibliography`](../fieldbibliography/) and [`FieldCitation`](../fieldcitation/) fields. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Gets or sets paths of MS Word built-in templates. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Gets or sets the field comparison expressions evaluator. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Gets or sets the current user information. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Gets or sets custom style separator for the \t switch in [`FieldToc`](../fieldtoc/) field. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Gets or sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Gets or sets a provider that returns a query result for the [`FieldDatabase`](../fielddatabase/) field. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Gets or sets a [`FieldIndexFormat`](./fieldindexformat/) that represents the formatting for the [`FieldIndex`](../fieldindex/) fields in the document. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Gets or sets a provider that returns a culture object specific for each particular field. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Specifies what culture to use to format the field result. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Gets or sets [`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementation |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Gets or sets [`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) implementation. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Gets or sets the file name of the document. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Gets or sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Gets or sets the culture to preprocess field values. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Allows to control how the field result is formatted. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Gets or sets the file name of the template used by the document. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Gets or sets the table of authorities categories. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Gets or sets the value indicating that number format is parsed using invariant culture or not |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Gets or sets the respondent to user prompts during field update. |

## Examples

Shows how to specify the source of the culture used for date formatting during a field update or mail merge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert two merge fields with German locale.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Set the current culture to US English after preserving its original value in a variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// This merge will use the current thread's culture to format the date, US English.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configure the next merge to source its culture value from the field code. The value of that culture will be German.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// The first merge result contains a date formatted in English, while the second one is in German.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restore the thread's original culture.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
