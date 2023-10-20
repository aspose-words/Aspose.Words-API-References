---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: FieldCollection Item fast egendom. Returnerar ett fält vid det angivna indexet i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

Returnerar ett fält vid det angivna indexet.

```csharp
public Field this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index i samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från baksidan av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder näst före sist och så vidare.

Om index är större än eller lika med antalet objekt i listan, returnerar detta en nollreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returnerar detta en nollreferens.

## Exempel

Visar hur man tar bort fält från en fältsamling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Nedan finns fyra sätt att ta bort fält från en fältsamling.
// 1 - Få ett fält för att ta bort sig själv:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Få samlingen för att ta bort ett fält som vi skickar till dess borttagningsmetod:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Ta bort ett fält från en samling vid ett index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Ta bort alla fält från samlingen på en gång:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Se även

* class [Field](../../field/)
* class [FieldCollection](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
