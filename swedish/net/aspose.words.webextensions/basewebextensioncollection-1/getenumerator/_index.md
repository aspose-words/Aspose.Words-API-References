---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Upptäck BaseWebExtensionCollection GetEnumerator-metoden för att enkelt iterera genom samlingar, vilket förbättrar din utvecklingseffektivitet och kodhantering.
type: docs
weight: 50
url: /sv/net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## BaseWebExtensionCollection&lt;T&gt;.GetEnumerator method

Returnerar en uppräknare som kan iterera genom en samling.

```csharp
public IEnumerator<T> GetEnumerator()
```

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
