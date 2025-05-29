---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Öğeleri dizine göre kolayca yönetmek için BaseWebExtensionCollection Item özelliğini keşfedin. Verimli veri işleme ile geliştirmenizi bugün basitleştirin!
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
| index | Öğenin sıfırdan başlayan indeksi. |

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
