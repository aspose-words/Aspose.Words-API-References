---
title: CustomXmlPropertyCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly remove properties from your CustomXmlPropertyCollection with our Remove method. Streamline your data management today!
type: docs
weight: 80
url: /net/aspose.words.markup/customxmlpropertycollection/remove/
---
## CustomXmlPropertyCollection.Remove method

Removes a property with the specified name from the collection.

```csharp
public void Remove(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The case-sensitive name of the property. |

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
