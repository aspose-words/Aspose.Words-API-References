---
title: FieldUserInitials.UserInitials
second_title: Aspose.Words for .NET API Referansı
description: FieldUserInitials mülk. Geçerli kullanıcının baş harflerini alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Geçerli kullanıcının baş harflerini alır veya ayarlar.

```csharp
public string UserInitials { get; set; }
```

### Örnekler

KULLANICI KILAVUZU alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir UserInformation nesnesi oluşturun ve oluşturduğumuz tüm alanlar için kullanıcı bilgilerinin kaynağı olarak ayarlayın.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Mevcut kullanıcının baş harflerini görüntülemek için bir KULLANICI ADILARI alanı oluşturun,
// yukarıda oluşturduğumuz UserInformation nesnesinden alınmıştır.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Bu özelliği, alanımızın UserInformation nesnesinde şu anda depolanan değeri geçersiz kılacak şekilde ayarlayabiliriz.
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
* ad alanı [Aspose.Words.Fields](../../fielduserinitials/)
* toplantı [Aspose.Words](../../../)


