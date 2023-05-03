---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
second_title: Aspose.Words for .NET API Reference
description: BaseWebExtensionCollection GetEnumerator method. Returns an enumerator that can iterate through a collection in C#.
type: docs
weight: 50
url: /net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## GetEnumerator method

Returns an enumerator that can iterate through a collection.

```csharp
public IEnumerator<T> GetEnumerator()
```

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
