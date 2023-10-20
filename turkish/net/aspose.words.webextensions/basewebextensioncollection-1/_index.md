---
title: BaseWebExtensionCollectionT Class
linktitle: BaseWebExtensionCollectionT
articleTitle: BaseWebExtensionCollectionT
second_title: Aspose.Words for .NET
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T sınıf. Temel sınıfTaskPaneCollection WebExtensionBindingCollection  WebExtensionPropertyCollection VeWebExtensionReferenceCollection koleksiyonlar C#'da.
type: docs
weight: 6700
url: /tr/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Temel sınıf[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) Ve[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) koleksiyonlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Office Eklentileriyle Çalışma](https://docs.aspose.com/words/net/work-with-office-add-ins/) dokümantasyon makalesi.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Parametre | Tanım |
| --- | --- |
| T | Bir koleksiyon öğesinin türü. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Belirtilen dizindeki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*T*) | Belirtilen öğeyi koleksiyona ekler. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Bir koleksiyonda yineleme yapabilen bir numaralandırıcıyı döndürür. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) | Belirtilen dizindeki öğeyi koleksiyondan kaldırır. |

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

* ad alanı [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* toplantı [Aspose.Words](../../)
