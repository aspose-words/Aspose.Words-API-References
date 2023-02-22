---
title: Item
second_title: Aspose.Words for .NET API Reference
description: FieldCollection property. Returns a field at the specified index in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

Returns a field at the specified index.

```csharp
public Field this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the collection. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples

Shows how to remove fields from a field collection.

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

// Below are four ways of removing fields from a field collection.
// 1 -  Get a field to remove itself:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 -  Get the collection to remove a field that we pass to its removal method:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 -  Remove a field from a collection at an index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 -  Remove all the fields from the collection at once:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### See Also

* class [Field](../../field/)
* class [FieldCollection](../)
* namespace [Aspose.Words.Fields](../../fieldcollection/)
* assembly [Aspose.Words](../../../)
