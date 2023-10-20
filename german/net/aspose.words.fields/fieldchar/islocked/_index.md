---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words für .NET
description: FieldChar IsLocked eigendom. Ruft ab oder legt fest ob das übergeordnete Feld gesperrt ist sollte sein Ergebnis nicht neu berechnen in C#.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Ruft ab oder legt fest, ob das übergeordnete Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen).

```csharp
public bool IsLocked { get; set; }
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

// Das Fassadenobjekt abrufen, das das Feld im Dokument darstellt.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Feld aktualisieren, um das aktuelle Datum anzuzeigen.
field.Update();
```

### Siehe auch

* class [FieldChar](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
