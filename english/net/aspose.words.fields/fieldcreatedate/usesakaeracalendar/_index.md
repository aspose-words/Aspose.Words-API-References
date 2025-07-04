---
title: FieldCreateDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words for .NET
description: Discover the FieldCreateDate UseSakaEraCalendar property to easily manage Saka Era calendar settings in your applications for enhanced date handling.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

Gets or sets whether to use the Saka Era calendar.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Examples

Shows how to use the CREATEDATE field to display the creation date/time of the document.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// We can use the CREATEDATE field to display the date and time of the creation of the document.
// Below are three different calendar types according to which the CREATEDATE field can display the date/time.
// 1 -  Islamic Lunar Calendar:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" CREATEDATE  \\h"));

// 2 -  Umm al-Qura calendar:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" CREATEDATE  \\u"));

// 3 -  Indian National Calendar:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" CREATEDATE  \\s"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### See Also

* class [FieldCreateDate](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
