---
title: Class PdfEncryptionDetails
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfEncryptionDetails sınıf. Bir PDF belgesi için şifreleme ve erişim izinleriyle ilgili ayrıntıları içerir.
type: docs
weight: 5180
url: /tr/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Bir PDF belgesi için şifreleme ve erişim izinleriyle ilgili ayrıntıları içerir.

```csharp
public class PdfEncryptionDetails
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/)(string, string) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Şifrelenmiş PDF belgesi için sahip parolasını belirtir. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değerDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Şifrelenmiş PDF belgesini açmak için gereken kullanıcı parolasını belirtir. |

### Örnekler

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Tüm izinleri reddederek başlayın.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Ek açıklamaların düzenlenmesine izin vermek için izinleri genişletin.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EncryptionDetails" özelliği ile şifrelemeyi etkinleştirin.
saveOptions.EncryptionDetails = encryptionDetails;

// Bu belgeyi açtığımızda, içeriğine erişmeden önce şifreyi sağlamamız gerekecek.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


