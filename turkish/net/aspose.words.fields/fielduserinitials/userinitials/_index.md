---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words for .NET
description: FieldUserInitials UserInitials mülk. Geçerli kullanıcının baş harflerini alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Geçerli kullanıcının baş harflerini alır veya ayarlar.

```csharp
public string UserInitials { get; set; }
```

## Örnekler

KULLANICI BAŞLANGIÇLARI alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir UserInformation nesnesi oluşturun ve onu, oluşturduğumuz tüm alanlar için kullanıcı bilgilerinin kaynağı olarak ayarlayın.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Geçerli kullanıcının baş harflerini görüntülemek için bir USERINITIALS alanı oluşturun,
// yukarıda oluşturduğumuz UserInformation nesnesinden alınmıştır.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Alanımızın şu anda UserInformation nesnesinde depolanan değeri geçersiz kılmasını sağlamak için bu özelliği ayarlayabiliriz.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Bu, UserInformation nesnesindeki değeri etkilemez.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Ayrıca bakınız

* class [FieldUserInitials](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
