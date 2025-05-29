---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldChar IsLocked, kontrollera omräkning av fält med lätthet. Förbättra ditt dokuments noggrannhet och effektivitet idag!
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Hämtar eller anger om det överordnade fältet är låst (ska inte beräkna om resultatet).

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

* class [FieldChar](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
