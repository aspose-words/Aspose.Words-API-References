---
title: BuiltInDocumentProperties.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: BuiltInDocumentProperties Title mülk. Belgenin başlığını alır veya ayarlar C#'da.
type: docs
weight: 290
url: /tr/net/aspose.words.properties/builtindocumentproperties/title/
---
## BuiltInDocumentProperties.Title property

Belgenin başlığını alır veya ayarlar.

```csharp
public string Title { get; set; }
```

## Örnekler

"Açıklama" kategorisinde yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Aşağıda, değerlerini belge gövdesinde görüntüleyebilen alanlara sahip dört yerleşik belge özelliği bulunmaktadır.
// 1 - AUTHOR alanını kullanarak görüntüleyebileceğimiz "Yazar" özelliği:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - TITLE alanını kullanarak görüntüleyebileceğimiz "Title" özelliği:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - SUBJECT alanını kullanarak görüntüleyebileceğimiz "Konu" özelliği:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - YORUMLAR alanını kullanarak görüntüleyebileceğimiz "Yorumlar" özelliği:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// "Kategori" yerleşik özelliğinin değerini görüntüleyebilecek bir alanı yok.
properties.Category = "My category";

// "Keywords" özelliğinin string değerini noktalı virgülle ayırarak bir belge için birden fazla anahtar kelime belirleyebiliriz.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Windows Explorer'da bu belgeye sağ tıklayıp bu özellikleri "Özellikler" --> "Detaylar".
// "Yazar" yerleşik özelliği "Origin" grubunda, diğerleri ise "Açıklama" grubundadır.
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
