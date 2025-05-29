---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Upptäck BaseWebExtensionCollections objektegenskap för att enkelt hantera objekt efter index. Förenkla din utveckling med effektiv datahantering idag!
type: docs
weight: 20
url: /sv/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Hämtar eller ställer in ett objekt vid det angivna indexet.

```csharp
public T this[int index] { get; set; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för objektet. |

## Exempel

Visar hur man arbetar med ett dokuments samling av webbtillägg.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Skriv ut alla egenskaper för dokumentets webbtillägg.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Ta bort webbtillägget.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Se även

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* namnutrymme [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* hopsättning [Aspose.Words](../../../)
