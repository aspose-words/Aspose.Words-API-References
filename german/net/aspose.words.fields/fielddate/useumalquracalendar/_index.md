---
title: FieldDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft FieldDate UseUmAlQuraCalendar, um Termine mit dem UmalQura-Kalender einfach zu verwalten. Optimieren Sie noch heute Ihre Terminverwaltung!
type: docs
weight: 50
url: /de/net/aspose.words.fields/fielddate/useumalquracalendar/
---
## FieldDate.UseUmAlQuraCalendar property

Ruft ab oder legt fest, ob der Um-al-Qura-Kalender verwendet werden soll.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Beispiele

Zeigt, wie DATE-Felder verwendet werden, um Daten entsprechend unterschiedlicher Kalendertypen anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir möchten, dass der Text im Dokument immer das richtige Datum anzeigt, können wir ein DATE-Feld verwenden.
// Unten sind drei Arten von Kulturkalendern aufgeführt, die ein DATE-Feld zum Anzeigen eines Datums verwenden kann.
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

// Fügen Sie ein DATE-Feld ein und legen Sie dessen Kalendertyp auf den zuletzt von der Hostanwendung verwendeten fest.
// In Microsoft Word ist der Typ der zuletzt im Dialogfeld Einfügen -> Text -> Datum und Uhrzeit verwendete.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Siehe auch

* class [FieldDate](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
