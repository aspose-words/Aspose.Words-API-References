---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Entdecken Sie die Item-Eigenschaft BaseWebExtensionCollection zur einfachen Verwaltung von Elementen nach Index. Vereinfachen Sie Ihre Entwicklung noch heute mit effizienter Datenverarbeitung!
type: docs
weight: 20
url: /de/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Ruft ein Element am angegebenen Index ab oder legt es fest.

```csharp
public T this[int index] { get; set; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Nullbasierter Index des Elements. |

## Beispiele

Zeigt, wie mit der Sammlung von Weberweiterungen eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Alle Eigenschaften der Weberweiterung des Dokuments drucken.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Entfernen Sie die Weberweiterung.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Siehe auch

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* namensraum [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../../)
