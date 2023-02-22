---
title: BaseWebExtensionCollection1.Item
second_title: Aspose.Words for .NET API Referansı
description: BaseWebExtensionCollection mülk. Belirtilen dizindeki bir öğeyi alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Belirtilen dizindeki bir öğeyi alır veya ayarlar.

```csharp
public T this[int index] { get; set; }
```

| Parametre | Tanım |
| --- | --- |
| index | Öğenin sıfır tabanlı dizini. |

### Örnekler

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
* ad alanı [Aspose.Words.WebExtensions](../../basewebextensioncollection-1/)
* toplantı [Aspose.Words](../../../)


