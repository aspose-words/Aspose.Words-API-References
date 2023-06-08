---
title: CustomXmlPropertyCollection.IndexOfKey
linktitle: IndexOfKey
articleTitle: IndexOfKey
second_title: Aspose.Words for .NET
description: CustomXmlPropertyCollection IndexOfKey method. Returns the zerobased index of the specified property in the collection in C#.
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

Assert.AreEqual(8, smartTags.Length);

// The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
// The properties of a "date"-type smart tag contain its year, month, and day.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// We can also access the properties in various ways, such as a key-value pair.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Below are three ways of removing elements from the properties collection.
// 1 -  Remove by index:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 -  Remove by name:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 -  Clear the entire collection at once:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### See Also

* class [CustomXmlPropertyCollection](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
