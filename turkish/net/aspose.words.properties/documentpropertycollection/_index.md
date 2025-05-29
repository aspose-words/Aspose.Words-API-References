---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: .NET için Aspose.Words
description: Yerleşik ve Özel Belge Özelliklerini etkili bir şekilde yönetmek için başvuracağınız Aspose.Words.Properties.DocumentPropertyCollection sınıfını keşfedin.
type: docs
weight: 5210
url: /tr/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Temel sınıf[`BuiltInDocumentProperties`](../builtindocumentproperties/) Ve[`CustomDocumentProperties`](../customdocumentproperties/) koleksiyonlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belge Özellikleriyle Çalışma](https://docs.aspose.com/words/net/work-with-document-properties/) belgeleme makalesi.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
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
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Koleksiyondan tüm özellikleri kaldırır. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Geri Döndürür`doğru` belirtilen ada sahip bir özellik koleksiyonda mevcutsa. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Bir özelliğin adına göre dizinini alır. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Belirtilen ada sahip bir özelliği koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Belirtilen dizindeki bir özelliği kaldırır. |

## Notlar

Özelliklerin adları büyük/küçük harfe duyarlı değildir.

Koleksiyondaki mülkler adlarına göre alfabetik olarak sıralanmıştır.

## Örnekler

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Belgedeki her özel özelliği yazdır.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// DOCPROPERTY alanını kullanarak özel bir özelliğin değerini görüntüleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Bu özel özellikleri Microsoft Word'de "Dosya" -> "Özellikler" > "Gelişmiş Özellikler" > "Özel" yoluyla bulabiliriz.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Tüm koleksiyonu bir defada boşalt:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)
