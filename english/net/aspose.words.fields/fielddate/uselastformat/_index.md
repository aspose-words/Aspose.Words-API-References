---
title: FieldDate.UseLastFormat
second_title: Aspose.Words for .NET API Reference
description: FieldDate property. Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field.

```csharp
public bool UseLastFormat { get; set; }
```

## Examples

Shows how to use DATE fields to display dates according to different kinds of calendars.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we want the text in the document always to display the correct date, we can use a DATE field.
// Below are three types of cultural calendars that a DATE field can use to display a date.
// 1 -  Islamic Lunar Calendar:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 -  Umm al-Qura calendar:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 -  Indian National Calendar:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Insert a DATE field and set its calendar type to the one last used by the host application.
// In Microsoft Word, the type will be the most recently used in the Insert -> Text -> Date and Time dialog box.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### See Also

* class [FieldDate](../)
* namespace [Aspose.Words.Fields](../../fielddate/)
* assembly [Aspose.Words](../../../)
