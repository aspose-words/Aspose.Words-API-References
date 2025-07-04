---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Discover the BaseWebExtensionCollection Item property to easily manage items by index. Simplify your development with efficient data handling today!
type: docs
weight: 20
url: /net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Gets or sets an item at the specified index.

```csharp
public T this[int index] { get; set; }
```

| Parameter | Description |
| --- | --- |
| index | Zero-based index of the item. |

## Examples

Shows how to work with a document's collection of web extensions.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.That(doc.WebExtensionTaskPanes.Count, Is.EqualTo(1));

// Print all properties of the document's web extension.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Remove the web extension.
doc.WebExtensionTaskPanes.Remove(0);

Assert.That(doc.WebExtensionTaskPanes.Count, Is.EqualTo(0));
```

### See Also

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* namespace [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* assembly [Aspose.Words](../../../)
