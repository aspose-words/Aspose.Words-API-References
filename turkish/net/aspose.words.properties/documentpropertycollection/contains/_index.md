---
title: DocumentPropertyCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: .NET için Aspose.Words
description: Verimli Contains metodumuzla DocumentPropertyCollection'da bir özelliğin var olup olmadığını keşfedin. Veri yönetiminizi bugün basitleştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.properties/documentpropertycollection/contains/
---
## DocumentPropertyCollection.Contains method

Geri Döndürür`doğru` belirtilen ada sahip bir özellik koleksiyonda mevcutsa.

```csharp
public bool Contains(string name)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Özelliğin büyük/küçük harfe duyarlı olmayan adı. |

### Geri dönüş değeri

`doğru` eğer mülk koleksiyonda mevcutsa;`YANLIŞ` aksi takdirde.

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

* class [DocumentPropertyCollection](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
