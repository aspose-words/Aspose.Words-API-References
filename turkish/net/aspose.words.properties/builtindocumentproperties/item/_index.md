---
title: BuiltInDocumentProperties.Item
second_title: Aspose.Words for .NET API Referansı
description: BuiltInDocumentProperties mülk. Bir değeri döndürürDocumentProperty özelliğin adına göre nesne.
type: docs
weight: 130
url: /tr/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Bir değeri döndürür[`DocumentProperty`](../../documentproperty/) özelliğin adına göre nesne.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parametre | Tanım |
| --- | --- |
| name | Alınacak özelliğin büyük/küçük harfe duyarlı olmayan adı. |

### Notlar

Özelliklerin dize adları, şurada mevcut olan typed özelliklerinin adlarına karşılık gelir.[`BuiltInDocumentProperties`](../).

Belgede bulunmayan bir özellik talep ederseniz ancak özelliğin name değeri geçerli bir yerleşik ad olarak tanınırsa, yeni bir[`DocumentProperty`](../../documentproperty/) oluşturulur, koleksiyona eklenir ve döndürülür. Yeni oluşturulan özelliğe varsayılan bir değer olarak atanır (boş dize, sıfır,`YANLIŞ` veya yerleşik özelliğin type türüne bağlı olarak DateTime.MinValue).

Belgede bulunmayan bir özellik talep ederseniz ve name yerleşik ad olarak tanınmıyorsa,`hükümsüz` Geri döndü.

### Örnekler

Özel belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Her belge, yerleşik özellikler gibi anahtar/değer çiftleri olan özel özelliklerin bir koleksiyonunu içerir.
 // Belgenin sabit bir yerleşik özellikler listesi vardır. Kullanıcı tüm özel özellikleri oluşturur.
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
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties/)
* toplantı [Aspose.Words](../../../)


