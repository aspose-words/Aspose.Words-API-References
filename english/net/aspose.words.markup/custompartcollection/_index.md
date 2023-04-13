---
title: CustomPartCollection Class
linktitle: CustomPartCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Markup.CustomPartCollection class. Represents a collection of CustomPart objects in C#.
type: docs
weight: 3740
url: /net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Represents a collection of [`CustomPart`](../custompart/) objects.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## Constructors

| Name | Description |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Gets or sets an item at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(CustomPart) | Adds an item to the collection. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Removes all elements from the collection. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Makes a deep copy of this collection and its items. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(int) | Removes an item at the specified index. |

## Remarks

You do not normally need to create instances of this class. You access custom parts related to the OOXML package via the [`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) property.

## Examples

Shows how to access a document's arbitrary custom parts collection.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Clone the second part, then add the clone to the collection.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

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

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### See Also

* class [CustomPart](../custompart/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
