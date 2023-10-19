---
title: BaseWebExtensionCollection1.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: BaseWebExtensionCollection Count mülk. Koleksiyonda yer alan öğelerin sayısını alır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.webextensions/basewebextensioncollection-1/count/
---
## BaseWebExtensionCollection&lt;T&gt;.Count property

Koleksiyonda yer alan öğelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Belgenin web uzantısının tüm özelliklerini yazdırın.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Web uzantısını kaldırın.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Ayrıca bakınız

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* ad alanı [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../../)
