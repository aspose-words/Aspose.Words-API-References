---
title: BaseWebExtensionCollectionT Class
linktitle: BaseWebExtensionCollectionT
articleTitle: BaseWebExtensionCollectionT
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WebExtensions.BaseWebExtensionCollection1T class, your essential tool for managing TaskPane and WebExtension collections efficiently.
type: docs
weight: 7550
url: /net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Base class for [`TaskPaneCollection`](../taskpanecollection/), [`WebExtensionBindingCollection`](../webextensionbindingcollection/), [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) and [`WebExtensionReferenceCollection`](../webextensionreferencecollection/) collections.

To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) documentation article.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Parameter | Description |
| --- | --- |
| T | Type of a collection item. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Gets or sets an item at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*T*) | Adds specified item to the collection. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Removes all elements from the collection. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Returns an enumerator that can iterate through a collection. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) | Removes the item at the specified index from the collection. |

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

* namespace [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assembly [Aspose.Words](../../)
