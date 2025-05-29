---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: .NET için Aspose.Words
description: Koleksiyonlar arasında kolayca yineleme yapmak, geliştirme verimliliğinizi ve kod yönetiminizi artırmak için BaseWebExtensionCollection GetEnumerator metodunu keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## BaseWebExtensionCollection&lt;T&gt;.GetEnumerator method

Bir koleksiyonda yineleme yapabilen bir numaralandırıcı döndürür.

```csharp
public IEnumerator<T> GetEnumerator()
```

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
