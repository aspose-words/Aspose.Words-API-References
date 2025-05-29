---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: .NET için Aspose.Words
description: Belge yazarlarının adlarını kolayca ayarlamak veya güncellemek, organizasyonu ve belge yönetimi verimliliğini artırmak için DefaultDocumentAuthor özelliğini yönetin.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Varsayılan belge yazarının adını alır veya ayarlar. Yazarın adı yerleşik belge özelliklerinde zaten belirtilmişse, bu seçenek dikkate alınmaz.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## Örnekler

Bir belge oluşturucusunun adını görüntülemek için AUTHOR alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR alanları sonuçlarını "Author" adlı yerleşik belge özelliğinden alır.
// Microsoft Word'de bir belge oluşturup kaydedersek,
// o özellikte kullanıcı adımız bulunacak.
// Ancak, Aspose.Words kullanarak programatik olarak bir belge oluşturursak,
// "Yazar" özelliği varsayılan olarak boş bir dize olacaktır.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// AUTHOR alanları için kullanılacak bir yedek yazar adı ayarlayın
// "Yazar" özelliği boş bir dize içeriyorsa.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Bir değer içeren bir AUTHOR alanını güncelleme
// bu değeri "Yazar" yerleşik özelliğine uygulayacaktır.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Bu özelliği değiştirip ardından AUTHOR alanını güncellediğinizde bu değer alana uygulanacaktır.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// "Ad" özelliğini değiştirdikten sonra bir AUTHOR alanını güncellersek,
// daha sonra alan yeni adı görüntüler ve yeni adı yerleşik özelliğe uygular.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR alanları DefaultDocumentAuthor özelliğini etkilemez.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
