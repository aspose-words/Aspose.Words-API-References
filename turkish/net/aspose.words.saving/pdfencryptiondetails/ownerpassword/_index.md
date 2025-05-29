---
title: PdfEncryptionDetails.OwnerPassword
linktitle: OwnerPassword
articleTitle: OwnerPassword
second_title: .NET için Aspose.Words
description: OwnerPassword özelliğinin şifrelenmiş PDF dosyalarınızı nasıl güvence altına aldığını ve yalnızca yetkili erişimi nasıl sağladığını keşfedin. Belgelerinizi zahmetsizce koruyun!
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Şifrelenmiş PDF belgesi için sahip parolasını belirtir.

```csharp
public string OwnerPassword { get; set; }
```

## Notlar

Sahip parolası, kullanıcının şifrelenmiş bir PDF belgesini belirtilen herhangi bir erişim kısıtlaması olmadan açmasına olanak tanır[`Permissions`](../permissions/).

Sahip şifresi kullanıcı şifresi ile aynı olamaz.

## Örnekler

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Açıklamaların düzenlenmesine izin vermek için izinleri genişletin.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// "EncryptionDetails" özelliği aracılığıyla şifrelemeyi etkinleştirin.
saveOptions.EncryptionDetails = encryptionDetails;

// Bu belgeyi açtığımızda, içeriğine erişmeden önce parolayı girmemiz gerekecektir.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
