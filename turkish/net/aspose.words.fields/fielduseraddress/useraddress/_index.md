---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: .NET için Aspose.Words
description: FieldUserAddress özelliğiyle kullanıcı posta adreslerini zahmetsizce yönetin. Gelişmiş deneyim için geçerli kullanıcı bilgilerini kolayca alın ve güncelleyin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Geçerli kullanıcının posta adresini alır veya ayarlar.

```csharp
public string UserAddress { get; set; }
```

## Örnekler

USERADDRESS alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir UserInformation nesnesi oluşturup, oluşturduğumuz tüm alanlar için kullanıcı bilgisinin kaynağı olarak ayarlayalım.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Mevcut kullanıcının adresini görüntülemek için bir USERADDRESS alanı oluşturun,
// Yukarıda oluşturduğumuz UserInformation nesnesinden alınmıştır.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// Alanımızın UserInformation nesnesinde depolanan değeri geçersiz kılmasını sağlamak için bu özelliği ayarlayabiliriz.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// Bu, UserInformation nesnesindeki değeri etkilemez.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### Ayrıca bakınız

* class [FieldUserAddress](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
