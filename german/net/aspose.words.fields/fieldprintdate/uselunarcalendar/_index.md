---
title: FieldPrintDate.UseLunarCalendar
second_title: Aspose.Words für .NET-API-Referenz
description: FieldPrintDate eigendom. Ruft ab oder legt fest ob der HijriMondkalender oder der hebräische Mondkalender verwendet werden soll.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldprintdate/uselunarcalendar/
---
## FieldPrintDate.UseLunarCalendar property

Ruft ab oder legt fest, ob der Hijri-Mondkalender oder der hebräische Mondkalender verwendet werden soll.

```csharp
public bool UseLunarCalendar { get; set; }
```

### Beispiele

Zeigt gelesene PRINTDATE-Felder an.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Wenn ein Dokument von einem Drucker gedruckt oder als PDF gedruckt (aber nicht als PDF exportiert) wird,
// PRINTDATE-Felder zeigen das Datum/die Uhrzeit des Druckvorgangs an.
// Wenn kein Druck stattgefunden hat, zeigen diese Felder "0/0/0000" an.
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, nach denen das Feld PRINTDATE
// kann Datum und Uhrzeit des letzten Druckvorgangs anzeigen.
// 1 - Islamischer Mondkalender:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Umm al-Qura Kalender:
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


