---
title: FieldPrintDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words för .NET
description: Hantera dina datum enkelt med FieldPrintDates Saka Era-kalenderfunktion. Växla enkelt för sömlös integration och förbättrad användarupplevelse.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

Hämtar eller anger om Saka-erans kalender ska användas.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Exempel

Visar lästa PRINTDATE-fält.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// När ett dokument skrivs ut av en skrivare eller skrivs ut som PDF (men inte exporteras till PDF),
// Fälten PRINTDATE visar utskriftens datum/tid.
// Om ingen utskrift har skett kommer dessa fält att visa "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Nedan följer tre olika kalendertyper enligt vilka PRINTDATE-fältet
// kan visa datum och tid för den senaste utskriften.
// 1 - Islamisk månkalender:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Umm al-Qura-kalendern:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Indisk nationalkalender:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Se även

* class [FieldPrintDate](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
