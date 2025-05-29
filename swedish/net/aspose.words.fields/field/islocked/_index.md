---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words för .NET
description: Upptäck IsLocked-egenskapen för fält – kontrollera omberäkning och förbättra dataintegriteten. Lås upp effektiv hantering av dina dataresultat idag!
type: docs
weight: 50
url: /sv/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om).

```csharp
public bool IsLocked { get; set; }
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

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
