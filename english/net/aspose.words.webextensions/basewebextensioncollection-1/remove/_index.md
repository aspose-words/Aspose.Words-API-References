---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET API Reference
description: BaseWebExtensionCollection Remove method. Removes the item at the specified index from the collection in C#.
type: docs
weight: 60
url: /net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Removes the item at the specified index from the collection.

```csharp
public void Remove(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the collection item. |

## Examples

Shows how to work with a document's collection of web extensions.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

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

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### See Also

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* namespace [Aspose.Words.WebExtensions](../../basewebextensioncollection-1/)
* assembly [Aspose.Words](../../../)
