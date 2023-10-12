---
title: CustomXmlSchemaCollection.Count
second_title: Aspose.Words for .NET API Referansı
description: CustomXmlSchemaCollection mülk. Koleksiyonda yer alan öğelerin sayısını alır.
type: docs
weight: 10
url: /tr/net/aspose.words.markup/customxmlschemacollection/count/
---
## CustomXmlSchemaCollection.Count property

Koleksiyonda yer alan öğelerin sayısını alır.

```csharp
public int Count { get; }
```

### Örnekler

XML şeması koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Bir XML şeması ilişkisi ekleyin.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Özel XML bölümünün XML şeması ilişkilendirme koleksiyonunu kopyalayın,
// ve ardından klona birkaç yeni şema ekleyin.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Şemaları numaralandırın ve her öğeyi yazdırın.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Aşağıda şemaları koleksiyondan kaldırmanın üç yolu verilmiştir.
// 1 - Bir şemayı dizine göre kaldırın:
schemas.RemoveAt(2);

// 2 - Bir şemayı değere göre kaldırın:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Koleksiyonu bir kerede boşaltmak için "Temizle" yöntemini kullanın.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Ayrıca bakınız

* class [CustomXmlSchemaCollection](../)
* ad alanı [Aspose.Words.Markup](../../customxmlschemacollection/)
* toplantı [Aspose.Words](../../../)


