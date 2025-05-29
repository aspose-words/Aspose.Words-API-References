---
title: UserInformation.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: UserInformation Name özelliğiyle kullanıcı profillerini zahmetsizce yönetin. Gelişmiş kişiselleştirme için kullanıcı adlarını kolayca alın veya güncelleyin.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/userinformation/name/
---
## UserInformation.Name property

Kullanıcının adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Örnekler

Kullanıcı ayrıntılarının nasıl ayarlanacağını ve alanlar kullanılarak nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir UserInformation nesnesi oluşturun ve bunu kullanıcı bilgilerini görüntüleyen alanlar için veri kaynağı olarak ayarlayın.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Kullanıcı adı, kullanıcı adı ve kullanıcı adresi değerlerini görüntüleyen kullanıcı adı alanlarını ekleyin
 // Yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özellikleri.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Alan seçenekleri nesnesinin ayrıca tüm belgelerdeki alanların başvurabileceği statik bir varsayılan kullanıcısı vardır.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### Ayrıca bakınız

* class [UserInformation](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
