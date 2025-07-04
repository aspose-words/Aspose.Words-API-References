---
title: FieldCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: Effortlessly remove fields from your document with the FieldCollection RemoveAt method. Streamline your data management today!
type: docs
weight: 60
url: /net/aspose.words.fields/fieldcollection/removeat/
---
## FieldCollection.RemoveAt method

Removes a field at the specified index from this collection and from the document.

```csharp
public void RemoveAt(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | An index into the collection. |

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

Assert.That(fields.Count, Is.EqualTo(6));

// Below are four ways of removing fields from a field collection.
// 1 -  Get a field to remove itself:
fields[0].Remove();
Assert.That(fields.Count, Is.EqualTo(5));

// 2 -  Get the collection to remove a field that we pass to its removal method:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.That(fields.Count, Is.EqualTo(4));

// 3 -  Remove a field from a collection at an index:
fields.RemoveAt(2);
Assert.That(fields.Count, Is.EqualTo(3));

// 4 -  Remove all the fields from the collection at once:
fields.Clear();
Assert.That(fields.Count, Is.EqualTo(0));
```

### See Also

* class [FieldCollection](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
