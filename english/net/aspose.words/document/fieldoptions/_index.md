---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words for .NET
description: Explore the Document FieldOptions property to manage field handling effectively. Discover unique options for enhanced document control and customization.
type: docs
weight: 130
url: /net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Gets a [`FieldOptions`](../../../aspose.words.fields/fieldoptions/) object that represents options to control field handling in the document.

```csharp
public FieldOptions FieldOptions { get; }
```

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
Assert.That(doc.Range.Text.Trim(), Is.EqualTo("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020"));

// Restore the thread's original culture.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### See Also

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
