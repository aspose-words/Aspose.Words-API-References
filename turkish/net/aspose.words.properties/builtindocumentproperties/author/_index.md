---
title: BuiltInDocumentProperties.Author
linktitle: Author
articleTitle: Author
second_title: .NET için Aspose.Words
description: BuiltInDocumentProperties Author özelliğiyle belge yazarlarını zahmetsizce yönetin. Daha iyi bir organizasyon için yazarın adını kolayca ayarlayın veya alın.
type: docs
weight: 10
url: /tr/net/aspose.words.properties/builtindocumentproperties/author/
---
## BuiltInDocumentProperties.Author property

Belgenin yazarının adını alır veya ayarlar.

```csharp
public string Author { get; set; }
```

## Örnekler

"Açıklama" kategorisindeki yerleşik belge özelliklerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Aşağıda, belge gövdesinde değerlerini görüntüleyebilen alanlara sahip dört yerleşik belge özelliği bulunmaktadır.
// 1 - AUTHOR alanını kullanarak görüntüleyebileceğimiz "Author" özelliği:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - TITLE alanını kullanarak görüntüleyebileceğimiz "Title" özelliği:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - SUBJECT alanını kullanarak görüntüleyebileceğimiz "Subject" özelliği:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - COMMENTS alanını kullanarak görüntüleyebileceğimiz "Comments" özelliği:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// "Kategori" yerleşik özelliğinin değerini görüntüleyebilecek bir alanı yoktur.
properties.Category = "My category";

// "Anahtar Sözcükler" özelliğinin dize değerini noktalı virgülle ayırarak bir belge için birden fazla anahtar sözcük belirleyebiliriz.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Bu belgeye Windows Gezgini'nde sağ tıklayıp "Özellikler" -> "Ayrıntılar" kısmından bu özellikleri bulabiliriz.
// "Yazar" yerleşik özelliği "Köken" grubunda, diğerleri ise "Açıklama" grubundadır.
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
