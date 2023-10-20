---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words for .NET
description: PdfSaveOptions EncryptionDetails mülk. Çıktı PDF belgesinin şifrelenmesine ilişkin ayrıntıları alır veya ayarlar C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Çıktı PDF belgesinin şifrelenmesine ilişkin ayrıntıları alır veya ayarlar.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Notlar

Varsayılan değer:`hükümsüz` ve çıktı belgesi şifrelenmeyecektir. Bu özellik geçerli bir değere ayarlandığında[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, sonra çıktı PDF belgesi şifrelenecektir.

PDF 1.7 tabanlı uyumluluğa (PDF/UA-1 dahil) kaydederken AES-128 şifreleme algoritması kullanılır. PDF 2.0 tabanlı uyumluluğa kaydederken AES-256 şifreleme algoritması kullanılır.

Şifreleme, PDF/A uyumluluğu nedeniyle yasaklanmıştır. PDF/A'ya kaydederken bu seçenek göz ardı edilecektir.

ContentCopyForAccessibility Çıktı belgesi şifrelenmişse PDF/UA uyumluluğu tarafından izin gereklidir. Bu izin, PDF/UA'ya kaydederken otomatik olarak kullanılacaktır.

ContentCopyForAccessibility izin PDF 2.0 formatında kullanımdan kaldırıldı. Bu izin, PDF 2.0'a kaydederken göz ardı edilecek.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
