---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words for .NET
description: FieldOptions DefaultDocumentAuthor mülk. Varsayılan belge yazarının adını alır veya ayarlar. Yazarın adı yerleşik belge özelliklerinde zaten belirtilmişse bu seçenek dikkate alınmaz C#'da.
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

Belgeyi oluşturan kişinin adını görüntülemek için YAZAR alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR alanları, sonuçlarını "Yazar" adı verilen yerleşik belge özelliğinden alır.
// Microsoft Word'de bir belge oluşturup kaydedersek,
// o özellikte kullanıcı adımız olacak.
// Ancak Aspose.Words kullanarak programlı olarak bir belge oluşturursak,
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

// Değer içeren bir AUTHOR alanının güncellenmesi
// bu değeri "Yazar" yerleşik özelliğine uygulayacaktır.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Bu özelliği değiştirip ardından AUTHOR alanını güncellemek bu değeri alana uygulayacaktır.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Bir AUTHOR alanını "Name" özelliğini değiştirdikten sonra güncellersek,
// daha sonra alan yeni adı gösterecek ve yeni adı yerleşik özelliğe uygulayacaktır.
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
