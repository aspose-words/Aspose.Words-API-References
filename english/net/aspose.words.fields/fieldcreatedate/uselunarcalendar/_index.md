---
title: FieldCreateDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words for .NET
description: Manage date formats effortlessly with the FieldCreateDate UseLunarCalendar property. Choose between Hijri and Hebrew Lunar calendars for precise scheduling.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldcreatedate/uselunarcalendar/
---
## FieldCreateDate.UseLunarCalendar property

Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar.

```csharp
public bool UseLunarCalendar { get; set; }
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
