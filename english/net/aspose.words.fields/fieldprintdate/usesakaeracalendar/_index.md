---
title: FieldPrintDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words for .NET
description: Manage your dates effortlessly with FieldPrintDate's Saka Era Calendar feature. Easily toggle for seamless integration and enhanced user experience.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

Gets or sets whether to use the Saka Era calendar.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Examples

Shows read PRINTDATE fields.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// When a document is printed by a printer or printed as a PDF (but not exported to PDF),
// PRINTDATE fields will display the print operation's date/time.
// If no printing has taken place, these fields will display "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.That(field.Result, Is.EqualTo("3/25/2020 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE "));

// Below are three different calendar types according to which the PRINTDATE field
// can display the date and time of the last printing operation.
// 1 -  Islamic Lunar Calendar:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.That(field.UseLunarCalendar, Is.True);
Assert.That(field.Result, Is.EqualTo("8/1/1441 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE  \\h"));

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 -  Umm al-Qura calendar:
Assert.That(field.UseUmAlQuraCalendar, Is.True);
Assert.That(field.Result, Is.EqualTo("8/1/1441 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE  \\u"));

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 -  Indian National Calendar:
Assert.That(field.UseSakaEraCalendar, Is.True);
Assert.That(field.Result, Is.EqualTo("1/5/1942 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE  \\s"));
```

### See Also

* class [FieldPrintDate](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
