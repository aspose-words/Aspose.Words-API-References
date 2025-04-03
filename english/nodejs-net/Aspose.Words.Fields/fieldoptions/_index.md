---
title: FieldOptions class
linktitle: FieldOptions class
articleTitle: FieldOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.FieldOptions class. Represents options to control field handling in a document"
type: docs
weight: 780
url: /nodejs-net/aspose.words.fields/fieldoptions/
---

## FieldOptions class

Represents options to control field handling in a document.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [bibliographyStylesProvider](./bibliographyStylesProvider/) | Gets or sets a provider that returns a bibliography style for the [FieldBibliography](../fieldbibliography/) and [FieldCitation](../fieldcitation/) fields. |
| [builtInTemplatesPaths](./builtInTemplatesPaths/) | Gets or sets paths of MS Word built-in templates. |
| [comparisonExpressionEvaluator](./comparisonExpressionEvaluator/) | Gets or sets the field comparison expressions evaluator. |
| [currentUser](./currentUser/) | Gets or sets the current user information. |
| [customTocStyleSeparator](./customTocStyleSeparator/) | Gets or sets custom style separator for the \\t switch in [FieldToc](../fieldtoc/) field. |
| [defaultDocumentAuthor](./defaultDocumentAuthor/) | Gets or sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered. |
| [fieldDatabaseProvider](./fieldDatabaseProvider/) | Gets or sets a provider that returns a query result for the [FieldDatabase](../fielddatabase/) field. |
| [fieldIndexFormat](./fieldIndexFormat/) | Gets or sets a [FieldOptions.fieldIndexFormat](./fieldIndexFormat/) that represents the formatting for the [FieldIndex](../fieldindex/) fields in the document. |
| [fieldUpdateCultureProvider](./fieldUpdateCultureProvider/) | Gets or sets a provider that returns a culture object specific for each particular field. |
| [fieldUpdateCultureSource](./fieldUpdateCultureSource/) | Specifies what culture to use to format the field result. |
| [fieldUpdatingCallback](./fieldUpdatingCallback/) | Gets or sets [IFieldUpdatingCallback](../ifieldupdatingcallback/) implementation |
| [fieldUpdatingProgressCallback](./fieldUpdatingProgressCallback/) | Gets or sets [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) implementation. |
| [fileName](./fileName/) | Gets or sets the file name of the document. |
| [isBidiTextSupportedOnUpdate](./isBidiTextSupportedOnUpdate/) | Gets or sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [legacyNumberFormat](./legacyNumberFormat/) | Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [resultFormatter](./resultFormatter/) | Allows to control how the field result is formatted. |
| [templateName](./templateName/) | Gets or sets the file name of the template used by the document. |
| [toaCategories](./toaCategories/) | Gets or sets the table of authorities categories. |
| [useInvariantCultureNumberFormat](./useInvariantCultureNumberFormat/) | Gets or sets the value indicating that number format is parsed using invariant culture or not |
| [userPromptRespondent](./userPromptRespondent/) | Gets or sets the respondent to user prompts during field update. |

### Examples

Shows how to specify the source of the culture used for date formatting during a field update or mail merge.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert two merge fields with German locale.
builder.font.localeId = new CultureInfo("de-DE").LCID;
builder.insertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.write(" - ");
builder.insertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Set the current culture to US English after preserving its original value in a variable.
CultureInfo currentCulture = Thread.currentThread.CurrentCulture;
Thread.currentThread.CurrentCulture = new CultureInfo("en-US");

// This merge will use the current thread's culture to format the date, US English.
doc.mailMerge.execute(new.at(] { "Date1" }, new object[) { new DateTime(2020, 1, 01) });

// Configure the next merge to source its culture value from the field code. The value of that culture will be German.
doc.fieldOptions.fieldUpdateCultureSource = aw.Fields.FieldUpdateCultureSource.FieldCode;
doc.mailMerge.execute(new.at(] { "Date2" }, new object[) { new DateTime(2020, 1, 01) });

// The first merge result contains a date formatted in English, while the second one is in German.
expect(doc.range.text.trim()).toEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020");

// Restore the thread's original culture.
Thread.currentThread.CurrentCulture = currentCulture;
```

### See Also

* module [Aspose.Words.Fields](../)

