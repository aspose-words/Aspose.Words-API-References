---
title: FieldSaveDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre Termine mühelos mit der Eigenschaft „FieldSaveDate“. Schalten Sie den UmalQura-Kalender einfach um, um Termine und Planungen zu optimieren.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldsavedate/useumalquracalendar/
---
## FieldSaveDate.UseUmAlQuraCalendar property

Ruft ab oder legt fest, ob der Um-al-Qura-Kalender verwendet werden soll.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## Beispiele

Zeigt, wie Sie mit dem Feld SAVEDATE das Datum/die Uhrzeit des letzten Speichervorgangs des Dokuments anzeigen, der mit Microsoft Word durchgeführt wurde.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Wir können das Feld SAVEDATE verwenden, um Datum und Uhrzeit des letzten Speichervorgangs im Dokument anzuzeigen.
// Der Speichervorgang, auf den sich diese Felder beziehen, ist das manuelle Speichern in einer Anwendung wie Microsoft Word,
// nicht die Save-Methode des Dokuments.
// Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, je nachdem, ob das Feld SAVEDATE Datum/Uhrzeit anzeigen kann.
// 1 - Islamischer Mondkalender:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura-Kalender:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Indischer Nationalkalender:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Die SAVEDATE-Felder beziehen ihre Datums-/Uhrzeitwerte aus der integrierten Eigenschaft LastSavedTime.
// Die Save-Methode des Dokuments aktualisiert diesen Wert nicht, wir können ihn jedoch trotzdem manuell aktualisieren.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Siehe auch

* class [FieldSaveDate](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
