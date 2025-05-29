---
title: FieldChar.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FieldChar IsDirty hjälper till att upprätthålla dokumentets noggrannhet genom att spåra ändringar, vilket säkerställer att dina fält alltid återspeglar de senaste uppdateringarna.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet.

```csharp
public bool IsDirty { get; set; }
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
