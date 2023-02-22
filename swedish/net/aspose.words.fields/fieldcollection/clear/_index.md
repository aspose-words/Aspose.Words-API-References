---
title: FieldCollection.Clear
second_title: Aspose.Words för .NET API Referens
description: FieldCollection metod. Tar bort alla fält i den här samlingen från dokumentet och från själva samlingen.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection.Clear method

Tar bort alla fält i den här samlingen från dokumentet och från själva samlingen.

```csharp
public void Clear()
```

### Exempel

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

* class [FieldCollection](../)
* namnutrymme [Aspose.Words.Fields](../../fieldcollection/)
* hopsättning [Aspose.Words](../../../)


