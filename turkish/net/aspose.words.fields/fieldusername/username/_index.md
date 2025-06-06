---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: .NET için Aspose.Words
description: FieldUserName özelliğiyle mevcut kullanıcının adını zahmetsizce yönetin. Kullanıcı deneyimini geliştirin ve etkileşimleri sorunsuz bir şekilde kişiselleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Geçerli kullanıcının adını Gest veya ayarlar.

```csharp
public string UserName { get; set; }
```

## Örnekler

USERNAME alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir UserInformation nesnesi oluşturup, oluşturduğumuz tüm alanlar için kullanıcı bilgisinin kaynağı olarak ayarlayalım.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Mevcut kullanıcının adını görüntülemek için bir KULLANICI ADI alanı oluşturun,
// Yukarıda oluşturduğumuz UserInformation nesnesinden alınmıştır.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Alanımızın UserInformation nesnesinde depolanan değeri geçersiz kılmasını sağlamak için bu özelliği ayarlayabiliriz.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Bu, UserInformation nesnesindeki değeri etkilemez.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Ayrıca bakınız

* class [FieldUserName](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
