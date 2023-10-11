---
title: PdfEncryptionDetails.OwnerPassword
second_title: Aspose.Words for .NET API Referansı
description: PdfEncryptionDetails mülk. Şifrelenmiş PDF belgesinin sahip parolasını belirtir.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Şifrelenmiş PDF belgesinin sahip parolasını belirtir.

```csharp
public string OwnerPassword { get; set; }
```

### Notlar

Sahip parolası, kullanıcının şifrelenmiş bir PDF belgesini, şurada belirtilen herhangi bir erişim kısıtlaması olmadan açmasına olanak tanır:[`Permissions`](../permissions/).

Sahip parolası kullanıcı parolasıyla aynı olamaz.

### Örnekler

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Ek açıklamaların düzenlenmesine izin vermek için izinleri genişletin.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// "EncryptionDetails" özelliği aracılığıyla şifrelemeyi etkinleştirin.
saveOptions.EncryptionDetails = encryptionDetails;

// Bu belgeyi açtığımızda içeriğine erişmeden önce şifreyi vermemiz gerekecek.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../pdfencryptiondetails/)
* toplantı [Aspose.Words](../../../)


