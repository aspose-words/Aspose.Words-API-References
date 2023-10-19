---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words for .NET
description: PdfEncryptionDetails UserPassword mülk. Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir.

```csharp
public string UserPassword { get; set; }
```

## Notlar

Görüntülemek üzere şifrelenmiş bir PDF belgesini açmak için kullanıcı parolası gerekecektir. 'de belirtilen izinler[`Permissions`](../permissions/) okuyucu yazılımı tarafından uygulanacaktır.

Kullanıcı şifresi olabilir`hükümsüz` veya boş dize, bu durumda PDF belgesini açarken kullanıcıdan şifre istenmeyecektir. Kullanıcı parolası, sahip parolasıyla aynı olamaz.

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

* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
