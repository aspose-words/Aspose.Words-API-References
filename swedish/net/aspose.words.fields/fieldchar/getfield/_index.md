---
title: FieldChar.GetField
linktitle: GetField
articleTitle: GetField
second_title: Aspose.Words för .NET
description: Upptäck GetField-metoden i FieldChar, hämta enkelt fält för optimal datahantering och förbättrad prestanda i dina applikationer.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

Returnerar ett fält för fältet char.

```csharp
public Field GetField()
```

### Returvärde

Ett fält för fältet tecken.

## Anmärkningar

En ny[`Field`](../../field/) objektet skapas varje gång metoden anropas.

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

* class [Field](../../field/)
* class [FieldChar](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
