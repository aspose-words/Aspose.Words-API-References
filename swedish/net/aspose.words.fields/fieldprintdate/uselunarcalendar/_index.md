---
title: FieldPrintDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words för .NET
description: FieldPrintDate UseLunarCalendar fast egendom. Hämtar eller ställer in om du vill använda Hijri Lunar eller Hebrew Lunar kalender i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

Hämtar eller ställer in om du vill använda Hijri Lunar eller Hebrew Lunar kalender.

```csharp
public bool UseLunarCalendar { get; set; }
```

## Exempel

Visar läs PRINTDATE-fält.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// När ett dokument skrivs ut av en skrivare eller skrivs ut som en PDF (men inte exporteras till PDF),
// PRINTDATE-fälten visar utskriftsoperationens datum/tid.
// Om ingen utskrift har skett kommer dessa fält att visa "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Nedan finns tre olika kalendertyper enligt vilka PRINTDATE-fältet
// kan visa datum och tid för den senaste utskriften.
// 1 - Islamisk månkalender:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Umm al-Qura kalender:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Indian National Calendar:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Se även

* class [FieldPrintDate](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
