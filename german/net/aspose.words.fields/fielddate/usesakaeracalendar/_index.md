---
title: FieldDate.UseSakaEraCalendar
second_title: Aspose.Words für .NET-API-Referenz
description: FieldDate eigendom. Ruft ab oder legt fest ob der SakaÄraKalender verwendet werden soll.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fielddate/usesakaeracalendar/
---
## FieldDate.UseSakaEraCalendar property

Ruft ab oder legt fest, ob der Saka-Ära-Kalender verwendet werden soll.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

### Beispiele

Zeigt, wie DATE-Felder verwendet werden, um Daten gemäß verschiedenen Kalenderarten anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir möchten, dass der Text im Dokument immer das richtige Datum anzeigt, können wir ein DATE-Feld verwenden.
// Unten sind drei Arten von Kulturkalendern aufgeführt, die ein DATE-Feld zur Anzeige eines Datums verwenden kann.
// 1 - Islamischer Mondkalender:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Umm al-Qura-Kalender:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Indischer Nationalkalender:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Ein DATE-Feld einfügen und seinen Kalendertyp auf den zuletzt von der Hostanwendung verwendeten festlegen.
// In Microsoft Word ist der Typ der zuletzt im Einfügen -> verwendete Typ. Text -> Dialogfeld „Datum und Uhrzeit“.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Siehe auch

* class [FieldDate](../)
* namensraum [Aspose.Words.Fields](../../fielddate/)
* Montage [Aspose.Words](../../../)


