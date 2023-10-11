---
title: PdfEncryptionDetails.PdfEncryptionDetails
second_title: Aspose.Words for .NET API Referansı
description: PdfEncryptionDetails inşaatçı. Bu sınıfın bir örneğini başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(string, string) {#constructor}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### Ayrıca bakınız

* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../pdfencryptiondetails/)
* toplantı [Aspose.Words](../../../)

---

## PdfEncryptionDetails(string, string, PdfPermissions) {#constructor_1}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
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


