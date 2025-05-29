---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: .NET için Aspose.Words
description: Özel belge özelliklerini zahmetsizce yönetmek için Aspose.Words.Properties.CustomDocumentProperties'i keşfedin. Belge yönetiminizi bugün geliştirin!
type: docs
weight: 5190
url: /tr/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Özel belge özelliklerinin bir koleksiyonu.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belge Özellikleriyle Çalışma](https://docs.aspose.com/words/net/work-with-document-properties/) belgeleme makalesi.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Koleksiyondaki öğelerin sayısını alır. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Bir[`DocumentProperty`](../documentproperty/) nesne index. tarafından |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Bir[`DocumentProperty`](../documentproperty/) nesnenin özelliğinin adına göre. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | Yeni bir özel belge özelliği oluştururBoolean veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | Yeni bir özel belge özelliği oluştururDateTime veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | Yeni bir özel belge özelliği oluştururDouble veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | Yeni bir özel belge özelliği oluştururNumber veri türü. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | Yeni bir özel belge özelliği oluştururString veri türü. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | İçerikle bağlantılı yeni bir özel belge özelliği oluşturur. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Koleksiyondan tüm özellikleri kaldırır. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Geri Döndürür`doğru` belirtilen ada sahip bir özellik koleksiyonda mevcutsa. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Bir özelliğin adına göre dizinini alır. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Belirtilen ada sahip bir özelliği koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Belirtilen dizindeki bir özelliği kaldırır. |

## Notlar

Her biri[`DocumentProperty`](../documentproperty/) nesne, bir kapsayıcı belgenin özel bir özelliğini temsil eder.

Özelliklerin adları büyük/küçük harfe duyarlı değildir.

Koleksiyondaki mülkler adlarına göre alfabetik olarak sıralanmıştır.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)
