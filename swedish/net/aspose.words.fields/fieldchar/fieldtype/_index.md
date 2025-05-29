---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words för .NET
description: Upptäck FieldChar FieldType-egenskapen, som visar fältets typ och förbättrar din datahantering och programmeringseffektivitet. Läs mer nu!
type: docs
weight: 10
url: /sv/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Returnerar fälttypen.

```csharp
public FieldType FieldType { get; }
```

## Exempel

Visar hur man arbetar med en FieldStart-nod.

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

// Hämta fasadobjektet som representerar fältet i dokumentet.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Uppdatera fältet för att visa aktuellt datum.
field.Update();
```

### Se även

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
