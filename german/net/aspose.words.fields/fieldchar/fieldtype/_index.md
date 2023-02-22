---
title: FieldChar.FieldType
second_title: Aspose.Words für .NET-API-Referenz
description: FieldChar eigendom. Gibt den Feldtyp zurück.
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Gibt den Feldtyp zurück.

```csharp
public FieldType FieldType { get; }
```

### Beispiele

Zeigt, wie mit einem FieldStart-Knoten gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Das Fassadenobjekt abrufen, das das Feld im Dokument darstellt.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Aktualisieren Sie das Feld, um das aktuelle Datum anzuzeigen.
field.Update();
```

### Siehe auch

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* namensraum [Aspose.Words.Fields](../../fieldchar/)
* Montage [Aspose.Words](../../../)


