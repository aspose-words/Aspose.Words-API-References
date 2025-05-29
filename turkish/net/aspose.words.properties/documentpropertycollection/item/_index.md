---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: DocumentPropertyCollection Item'ımızla DocumentProperty nesnelerine zahmetsizce erişin. Sorunsuz belge yönetimi için özellikleri adlarına göre alın.
type: docs
weight: 20
url: /tr/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Bir[`DocumentProperty`](../../documentproperty/) nesnenin özelliğinin adına göre.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Parametre | Tanım |
| --- | --- |
| name | Alınacak özelliğin büyük/küçük harfe duyarlı olmayan adı. |

## Notlar

İade`hükümsüz` Belirtilen isimde bir özellik bulunamazsa.

## Örnekler

Tarih ve saat içeren özel bir belge özelliğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### Ayrıca bakınız

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Bir[`DocumentProperty`](../../documentproperty/) nesne index. tarafından

```csharp
public DocumentProperty this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Sıfır tabanlı endeks[`DocumentProperty`](../../documentproperty/) geri almak. |

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
