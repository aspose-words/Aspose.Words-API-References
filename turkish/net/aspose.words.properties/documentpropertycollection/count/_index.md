---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Verimli veri yönetimi için koleksiyonunuzdaki öğelerin sayısını zahmetsizce almak üzere DocumentPropertyCollection Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

Koleksiyondaki öğelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Özel belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Her belge, yerleşik özellikler gibi anahtar-değer çiftleri olan bir dizi özel özellik içerir.
 // Belgenin yerleşik özelliklerin sabit bir listesi vardır. Kullanıcı tüm özel özellikleri oluşturur.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Ayrıca bakınız

* class [DocumentPropertyCollection](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
