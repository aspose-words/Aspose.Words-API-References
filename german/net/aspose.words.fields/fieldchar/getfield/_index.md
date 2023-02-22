---
title: FieldChar.GetField
second_title: Aspose.Words für .NET-API-Referenz
description: FieldChar methode. Gibt ein Feld für das Feld char. zurück
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

Gibt ein Feld für das Feld char. zurück

```csharp
public Field GetField()
```

### Rückgabewert

Ein Feld für das Feld char.

### Bemerkungen

Ein neues[`Field`](../../field/) -Objekt wird bei jedem Aufruf der Methode erstellt.

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

* class [Field](../../field/)
* class [FieldChar](../)
* namensraum [Aspose.Words.Fields](../../fieldchar/)
* Montage [Aspose.Words](../../../)


