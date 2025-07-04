---
title: CustomPartCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: Effortlessly enhance your project with the CustomPartCollection Add method—quickly add items to your collection for seamless integration and efficiency.
type: docs
weight: 40
url: /net/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection.Add method

Adds an item to the collection.

```csharp
public void Add(CustomPart part)
```

| Parameter | Type | Description |
| --- | --- | --- |
| part | CustomPart | The item to add. |

## Examples

Shows how to access a document's arbitrary custom parts collection.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.That(doc.PackageCustomParts.Count, Is.EqualTo(2));

// Clone the second part, then add the clone to the collection.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.That(doc.PackageCustomParts.Count, Is.EqualTo(3));

// Enumerate over the collection and print every part.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// We can remove elements from this collection individually, or all at once.
doc.PackageCustomParts.RemoveAt(2);

Assert.That(doc.PackageCustomParts.Count, Is.EqualTo(2));

doc.PackageCustomParts.Clear();

Assert.That(doc.PackageCustomParts.Count, Is.EqualTo(0));
```

### See Also

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
