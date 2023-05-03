---
title: CustomPart Class
linktitle: CustomPart
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Markup.CustomPart class. Represents a custom arbitrary content part that is not defined by the ISO/IEC 29500 standard in C#.
type: docs
weight: 3810
url: /net/aspose.words.markup/custompart/
---
## CustomPart class

Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class CustomPart
```

## Constructors

| Name | Description |
| --- | --- |
| [CustomPart](custompart/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Specifies the content type of this custom part. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Contains the data of this custom part. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | False if this custom part is stored inside the OOXML package. True if this custom part is an external target. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Gets or sets this part's absolute name within the OOXML package or the target URL. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Gets or sets the relationship type from the parent part to this custom part. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Makes a "deep enough" copy of the object. Does not duplicate the bytes of the [`Data`](./data/) value. |

## Remarks

This class represents an OOXML part that is a target of an "unknown relationship". All relationships not defined within ISO/IEC 29500 are considered "unknown relationships". Unknown relationships are permitted within an Office Open XML document provided that they conform to relationship markup guidelines.

Microsoft Word preserves custom parts during open/save cycles. Some additional info can be found here http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words also roundtrips custom parts and in addition, allows to programmatically access such parts via the `CustomPart` and [`CustomPartCollection`](../custompartcollection/) objects.

Do not confuse custom parts with Custom XML Data. Use [`CustomXmlPart`](../customxmlpart/) if you need to access Custom XML Data.

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

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
