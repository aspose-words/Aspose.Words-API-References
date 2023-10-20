---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfEncryptionDetails sınıf. Bir PDF belgesinin şifrelenmesine ve erişim izinlerine ilişkin ayrıntıları içerir C#'da.
type: docs
weight: 5460
url: /tr/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Bir PDF belgesinin şifrelenmesine ve erişim izinlerine ilişkin ayrıntıları içerir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Koruyun veya Şifreleyin](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) dokümantasyon makalesi.

```csharp
public class PdfEncryptionDetails
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | Bu sınıfın bir örneğini başlatır. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Şifrelenmiş PDF belgesinin sahip parolasını belirtir. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Şifrelenmiş bir PDF belgesinde kullanıcıya izin verilen işlemleri belirtir. Varsayılan değer:DisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir. |

## Örnekler

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
