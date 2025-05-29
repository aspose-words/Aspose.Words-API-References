---
title: PdfEncryptionDetails.Permissions
linktitle: Permissions
articleTitle: Permissions
second_title: .NET için Aspose.Words
description: Şifrelenmiş PDF'lerde kullanıcı işlemlerini tanımlayan PdfEncryptionDetails Permissions özelliğini keşfedin. Özelleştirilebilir erişimle güvenli belge yönetiminin kilidini açın!
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değerDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
