---
title: Class UserInformation
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.UserInformation sınıf. Kullanıcı hakkındaki bilgileri belirtir.
type: docs
weight: 2790
url: /tr/net/aspose.words.fields/userinformation/
---
## UserInformation class

Kullanıcı hakkındaki bilgileri belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

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

### Örnekler

Kullanıcı ayrıntılarının nasıl ayarlanacağını ve alanları kullanarak bunların nasıl görüntüleneceğini gösterir.

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

// değerlerini görüntüleyen USERNAME, USERINITIALS ve USERAADDRESS alanlarını ekleyin
 // yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özellikleri.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Alan seçenekleri nesnesi aynı zamanda tüm belgelerdeki alanların başvurabileceği statik bir varsayılan kullanıcıya da sahiptir.
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


