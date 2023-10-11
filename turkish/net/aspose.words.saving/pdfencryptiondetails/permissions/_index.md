---
title: PdfEncryptionDetails.Permissions
second_title: Aspose.Words for .NET API Referansı
description: PdfEncryptionDetails mülk. Şifrelenmiş bir PDF belgesinde kullanıcıya izin verilen işlemleri belirtir. Varsayılan değerDisallowAll .
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Şifrelenmiş bir PDF belgesinde kullanıcıya izin verilen işlemleri belirtir. Varsayılan değer:DisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../pdfencryptiondetails/)
* toplantı [Aspose.Words](../../../)


