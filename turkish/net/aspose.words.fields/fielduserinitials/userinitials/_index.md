---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: .NET için Aspose.Words
description: Kullanıcı baş harflerini zahmetsizce yönetmek, kişiselleştirmeyi ve kullanıcı deneyimini geliştirmek için FieldUserInitials özelliğine erişin ve özelleştirin.
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

USERINITIALS alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir UserInformation nesnesi oluşturup, oluşturduğumuz tüm alanlar için kullanıcı bilgisinin kaynağı olarak ayarlayalım.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Mevcut kullanıcının baş harflerini görüntülemek için bir USERINITIALS alanı oluşturun,
// Yukarıda oluşturduğumuz UserInformation nesnesinden alınmıştır.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Alanımızın UserInformation nesnesinde depolanan değeri geçersiz kılmasını sağlamak için bu özelliği ayarlayabiliriz.
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
