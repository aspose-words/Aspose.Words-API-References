---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Sezgisel Remove yöntemimizle BaseWebExtensionCollection'ınızdan öğeleri zahmetsizce kaldırın. Veri yönetiminizi bugün kolaylaştırın!
type: docs
weight: 60
url: /tr/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Belirtilen dizindeki öğeyi koleksiyondan kaldırır.

```csharp
public void Remove(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Koleksiyon öğesinin sıfır tabanlı endeksi. |

## Örnekler

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Belgenin web uzantısının tüm özelliklerini yazdır.
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
