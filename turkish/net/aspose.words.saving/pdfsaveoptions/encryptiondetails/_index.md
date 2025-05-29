---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: .NET için Aspose.Words
description: PDF şifreleme ayarlarını kolayca yapılandırmak ve belgelerinizin güvenli ve korumalı kalmasını sağlamak için PdfSaveOptions'ın EncryptionDetails özelliğini keşfedin.
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

Varsayılan değer:`hükümsüz` ve çıktı belgesi şifrelenmeyecektir. Bu özellik geçerli bir değere ayarlandığında[`PdfEncryptionDetails`](../../pdfencryptiondetails/)nesne, ise çıktı PDF belgesi şifrelenecektir.

PDF 1.7 uyumluluğa (PDF/UA-1 dahil) kaydederken AES-128 şifreleme algoritması kullanılır. PDF 2.0 uyumluluğa kaydederken AES-256 şifreleme algoritması kullanılır.

Şifreleme PDF/A uyumluluğu tarafından yasaklanmıştır. Bu seçenek PDF/A'ya kaydedilirken göz ardı edilecektir.

ContentCopyForAccessibility Çıkış belgesi şifrelenmişse PDF/UA uyumluluğu tarafından izin gereklidir. Bu izin PDF/UA'ya kaydederken otomatik olarak kullanılacaktır.

ContentCopyForAccessibility PDF 2.0 formatında izin kullanım dışıdır. Bu izin, PDF 2.0'a kaydedilirken göz ardı edilecektir.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
