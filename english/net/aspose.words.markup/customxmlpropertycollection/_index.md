---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Markup.CustomXmlPropertyCollection, a powerful tool for managing custom XML attributes and smart tag properties efficiently.
type: docs
weight: 4630
url: /net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Represents a collection of custom XML attributes or smart tag properties.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Gets a property with the specified name. (2 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Adds a property to the collection. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Removes all elements from the collection. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Determines whether the collection contains a property with the given name. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Returns the zero-based index of the specified property in the collection. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Removes a property with the specified name from the collection. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Removes a property at the specified index. |

## Remarks

Items are [`CustomXmlProperty`](../customxmlproperty/) objects.

## Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
// such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
// In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
// In our input document, there are three objects that Microsoft Word registered as smart tags.
// Smart tags may be nested, so this collection contains more.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.That(smartTags.Length, Is.EqualTo(8));

// The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
// The properties of a "date"-type smart tag contain its year, month, and day.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.That(properties.Count, Is.EqualTo(4));

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.That(enumerator.Current.Uri, Is.EqualTo(""));
    }
}

// We can also access the properties in various ways, such as a key-value pair.
Assert.That(properties.Contains("Day"), Is.True);
Assert.That(properties["Day"].Value, Is.EqualTo("22"));
Assert.That(properties[2].Value, Is.EqualTo("2003"));
Assert.That(properties.IndexOfKey("Month"), Is.EqualTo(1));

// Below are three ways of removing elements from the properties collection.
// 1 -  Remove by index:
properties.RemoveAt(3);

Assert.That(properties.Count, Is.EqualTo(3));

// 2 -  Remove by name:
properties.Remove("Year");

Assert.That(properties.Count, Is.EqualTo(2));

// 3 -  Clear the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [CustomXmlProperty](../customxmlproperty/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
