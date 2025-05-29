---
title: UserInformation.DefaultUser
linktitle: DefaultUser
articleTitle: DefaultUser
second_title: .NET için Aspose.Words
description: Kusursuz kullanıcı bilgisi yönetimi için DefaultUser özelliğini keşfedin. Kullanımı kolay özelliklerimizle uygulamanızın verimliliğini artırın!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/userinformation/defaultuser/
---
## UserInformation.DefaultUser property

Varsayılan kullanıcı bilgisi.

```csharp
public static UserInformation DefaultUser { get; }
```

## Notlar

Şunu kullanın:[`CurrentUser`](../../fieldoptions/currentuser/) tek bir belge için kullanıcı bilgilerini belirtmek için özellik.

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
