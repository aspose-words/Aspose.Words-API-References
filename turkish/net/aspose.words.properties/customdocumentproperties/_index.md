---
title: Class CustomDocumentProperties
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Properties.CustomDocumentProperties sınıf. Özel belge özelliklerinden oluşan bir koleksiyon.
type: docs
weight: 4460
url: /tr/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Özel belge özelliklerinden oluşan bir koleksiyon.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belge Özellikleriyle Çalışma](https://docs.aspose.com/words/net/work-with-document-properties/) dokümantasyon makalesi.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Koleksiyondaki öğelerin sayısını alır. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Bir değeri döndürür[`DocumentProperty`](../documentproperty/) indekse göre nesne. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Bir değeri döndürür[`DocumentProperty`](../documentproperty/) özelliğin adına göre nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(string, bool) | Yeni bir özel belge özelliği oluşturur.Boolean veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(string, DateTime) | Yeni bir özel belge özelliği oluşturur.DateTime veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(string, double) | Yeni bir özel belge özelliği oluşturur.Double veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(string, int) | Yeni bir özel belge özelliği oluşturur.Number veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(string, string) | Yeni bir özel belge özelliği oluşturur.String veri türü. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(string, string) | İçeriğe bağlı yeni bir özel belge özelliği oluşturur. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Koleksiyondaki tüm özellikleri kaldırır. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | İadeler`doğru` koleksiyonda belirtilen ada sahip bir özellik mevcutsa. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Bir özelliğin dizinini ada göre alır. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Belirtilen ada sahip bir özelliği koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Belirtilen dizindeki bir özelliği kaldırır. |

### Notlar

Her biri[`DocumentProperty`](../documentproperty/) nesne bir kapsayıcı belgenin özel bir özelliğini temsil eder.

Özelliklerin adları büyük/küçük harfe duyarlı değildir.

Koleksiyondaki özellikler ada göre alfabetik olarak sıralanmıştır.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)


