---
title: CustomXmlPropertyCollection.IndexOfKey
linktitle: IndexOfKey
articleTitle: IndexOfKey
second_title: Aspose.Words for .NET
description: Discover the CustomXmlPropertyCollection IndexOfKey method to easily find the zero-based index of any property in your collection. Enhance your coding efficiency!
type: docs
weight: 70
url: /net/aspose.words.markup/customxmlpropertycollection/indexofkey/
---
## CustomXmlPropertyCollection.IndexOfKey method

Returns the zero-based index of the specified property in the collection.

```csharp
public int IndexOfKey(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The case-sensitive name of the property. |

### Return Value

The zero based index. Negative value if not found.

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

* class [CustomXmlPropertyCollection](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
