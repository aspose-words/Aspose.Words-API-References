---
title: FieldSaveDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words for .NET
description: FieldSaveDate UseLunarCalendar property. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldsavedate/uselunarcalendar/
---
## FieldSaveDate.UseLunarCalendar property

Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Examples

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// We can use the SAVEDATE field to display the last save operation's date and time on the document.
// The save operation that these fields refer to is the manual save in an application like Microsoft Word,
// not the document's Save method.
// Below are three different calendar types according to which the SAVEDATE field can display the date/time.
// 1 -  Islamic Lunar Calendar:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 -  Umm al-Qura calendar:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 -  Indian National calendar:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
// The document's Save method will not update this value, but we can still update it manually.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### See Also

* class [FieldSaveDate](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
