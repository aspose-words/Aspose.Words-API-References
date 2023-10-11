---
title: FieldPrintDate.UseSakaEraCalendar
second_title: Aspose.Words für .NET-API-Referenz
description: FieldPrintDate eigendom. Ruft ab oder legt fest ob der SakaÄraKalender verwendet werden soll.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

Ruft ab oder legt fest, ob der Saka-Ära-Kalender verwendet werden soll.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

### Beispiele

Zeigt gelesene PRINTDATE-Felder an.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Wenn ein Dokument von einem Drucker gedruckt oder als PDF gedruckt (aber nicht als PDF exportiert) wird,
// PRINTDATE-Felder zeigen Datum und Uhrzeit des Druckvorgangs an.
// Wenn kein Ausdruck stattgefunden hat, wird in diesen Feldern „0/0/0000“ angezeigt.
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Unten sind drei verschiedene Kalendertypen aufgeführt, entsprechend dem PRINTDATE-Feld
// kann Datum und Uhrzeit des letzten Druckvorgangs anzeigen.
// 1 - Islamischer Mondkalender:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Umm al-Qura-Kalender:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Indischer Nationalkalender:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Siehe auch

* class [FieldPrintDate](../)
* namensraum [Aspose.Words.Fields](../../fieldprintdate/)
* Montage [Aspose.Words](../../../)


