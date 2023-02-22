---
title: UserInformation.DefaultUser
second_title: Aspose.Words for .NET API Referansı
description: UserInformation mülk. Varsayılan kullanıcı bilgisi.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/userinformation/defaultuser/
---
## UserInformation.DefaultUser property

Varsayılan kullanıcı bilgisi.

```csharp
public static UserInformation DefaultUser { get; }
```

### Notlar

[`CurrentUser`](../../fieldoptions/currentuser/)tek belge için kullanıcı bilgilerini belirtme özelliği.

### Örnekler

Kullanıcı ayrıntılarının nasıl ayarlanacağını ve alanları kullanarak nasıl görüntüleneceğini gösterir.

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

// değerlerini görüntüleyen USERNAME, USERINITIALS ve USERADDRESS alanlarını girin
// yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özellikleri. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Alan seçenekleri nesnesi ayrıca tüm belgelerdeki alanların başvurabileceği statik bir varsayılan kullanıcıya sahiptir.
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
* ad alanı [Aspose.Words.Fields](../../userinformation/)
* toplantı [Aspose.Words](../../../)


