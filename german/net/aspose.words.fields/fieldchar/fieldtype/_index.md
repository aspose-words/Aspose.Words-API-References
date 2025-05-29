---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldChar-Eigenschaft „FieldType“, die den Feldtyp anzeigt und so Ihre Datenverwaltung und Programmiereffizienz verbessert. Jetzt mehr erfahren!
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Gibt den Typ des Felds zurück.

```csharp
public FieldType FieldType { get; }
```

## Beispiele

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

// Ruft das Fassadenobjekt ab, das das Feld im Dokument darstellt.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Aktualisieren Sie das Feld, um das aktuelle Datum anzuzeigen.
field.Update();
```

### Siehe auch

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
