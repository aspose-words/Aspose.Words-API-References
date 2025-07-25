---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words for .NET
description: Manage custom parts in your OOXML package effortlessly. Access and modify linked content with ease for enhanced document flexibility and functionality.
type: docs
weight: 320
url: /net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## Remarks

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [`CustomXmlParts`](../customxmlparts/) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be `null`.

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

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
