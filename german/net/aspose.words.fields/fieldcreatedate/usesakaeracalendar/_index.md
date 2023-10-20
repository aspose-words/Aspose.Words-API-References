---
title: FieldCreateDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: Aspose.Words für .NET
description: FieldCreateDate UseSakaEraCalendar eigendom. Ruft ab oder legt fest ob der SakaÄraKalender verwendet werden soll in C#.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

Ruft ab oder legt fest, ob der Saka-Ära-Kalender verwendet werden soll.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Beispiele

Zeigt, wie das Feld CREATEDATE verwendet wird, um das Erstellungsdatum und die Erstellungszeit des Dokuments anzuzeigen.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Wir können das Feld CREATEDATE verwenden, um Datum und Uhrzeit der Erstellung des Dokuments anzuzeigen.
// Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, nach denen das CREATEDATE-Feld Datum/Uhrzeit anzeigen kann.
// 1 - Islamischer Mondkalender:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura-Kalender:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Indischer Nationalkalender:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Siehe auch

* class [FieldCreateDate](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
