---
title: FieldPrintDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
second_title: Aspose.Words for .NET API Reference
description: FieldPrintDate UseUmAlQuraCalendar property. Gets or sets whether to use the UmalQura calendar in C#.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldprintdate/useumalquracalendar/
---
## UseUmAlQuraCalendar property

Gets or sets whether to use the Um-al-Qura calendar.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Examples

Shows read PRINTDATE fields.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// When a document is printed by a printer or printed as a PDF (but not exported to PDF),
// PRINTDATE fields will display the print operation's date/time.
// If no printing has taken place, these fields will display "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Below are three different calendar types according to which the PRINTDATE field
// can display the date and time of the last printing operation.
// 1 -  Islamic Lunar Calendar:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 -  Umm al-Qura calendar:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 -  Indian National Calendar:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### See Also

* class [FieldPrintDate](../)
* namespace [Aspose.Words.Fields](../../fieldprintdate/)
* assembly [Aspose.Words](../../../)
