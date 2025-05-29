---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: .NET için Aspose.Words
description: Güvenli PDF şifreleme örneklerini kolayca başlatmak için PdfEncryptionDetails oluşturucusunu keşfedin. Güçlü aracımızla belge korumanızı geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(*string, string*) {#constructor}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### Ayrıca bakınız

* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## PdfEncryptionDetails(*string, string, [PdfPermissions](../../pdfpermissions/)*) {#constructor_1}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
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
