---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: .NET için Aspose.Words
description: Güvenli PDF şifrelemesi ve özelleştirilebilir erişim izinleri için Aspose.Words.PdfEncryptionDetails'ı keşfedin; belgelerinizin korunmasını sağlayın.
type: docs
weight: 6250
url: /tr/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Bir PDF belgesi için şifreleme ve erişim izinlerine ilişkin ayrıntıları içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Koruyun veya Şifreleyin](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) belgeleme makalesi.

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
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Şifrelenmiş PDF belgesi için sahip parolasını belirtir. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değerDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Şifrelenmiş PDF belgesini açmak için gereken kullanıcı parolasını belirtir. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
