---
title: UserInformation Class
linktitle: UserInformation
articleTitle: UserInformation
second_title: .NET için Aspose.Words
description: Uygulamalarınızda kullanıcı ayrıntılarını etkili bir şekilde yönetmek ve belge işlemeyi geliştirmek için Aspose.Words.Fields.UserInformation sınıfını keşfedin.
type: docs
weight: 3200
url: /tr/net/aspose.words.fields/userinformation/
---
## UserInformation class

Kullanıcı hakkında bilgi belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class UserInformation
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [UserInformation](userinformation/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | Varsayılan kullanıcı bilgisi. |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | Kullanıcının posta adresini alır veya ayarlar. |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | Kullanıcının baş harflerini alır veya ayarlar. |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | Kullanıcının adını alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
