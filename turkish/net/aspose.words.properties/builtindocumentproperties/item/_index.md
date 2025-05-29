---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: BuiltInDocumentProperties Item özelliğiyle DocumentProperty nesnelerine zahmetsizce erişin. Belge yönetiminizi bugün kolaylaştırın!
type: docs
weight: 140
url: /tr/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Bir[`DocumentProperty`](../../documentproperty/) nesnenin özelliğinin adına göre.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parametre | Tanım |
| --- | --- |
| name | Alınacak özelliğin büyük/küçük harfe duyarlı olmayan adı. |

## Notlar

Özelliklerin dize adları, typed özelliğinin adlarına karşılık gelir.[`BuiltInDocumentProperties`](../).

Belgede bulunmayan bir özelliği talep ederseniz ancak özelliğin name değeri geçerli bir yerleşik ad olarak tanınırsa, yeni bir[`DocumentProperty`](../../documentproperty/) oluşturulur, koleksiyona eklenir ve döndürülür. Yeni oluşturulan özelliğe varsayılan bir değer atanır (boş dize, sıfır,`YANLIŞ` veya yerleşik özelliğin type değerine bağlı olarak DateTime.MinValue).

Belgede bulunmayan bir özelliği talep ederseniz ve name yerleşik bir ad olarak tanınmıyorsa,`hükümsüz` iade edilir.

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
* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
