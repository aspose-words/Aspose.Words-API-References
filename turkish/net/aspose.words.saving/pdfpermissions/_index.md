---
title: Enum PdfPermissions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfPermissions Sıralama. Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir.
type: docs
weight: 5230
url: /tr/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir.

```csharp
[Flags]
public enum PdfPermissions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| DisallowAll | `0` | PDF belgesindeki tüm işlemlere izin vermez. Bu varsayılan değerdir. |
| AllowAll | `FFFF` | PDF belgesindeki tüm işlemlere izin verir. |
| ContentCopy | `10` | Tarafından denetlenen dışındaki işlemlerle belgeden metin ve grafikleri kopyalayın veya başka bir şekilde çıkarın.ContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Metin ve grafikleri ayıklayın (engelli kullanıcılara erişilebilirliği desteklemek veya başka amaçlar için). |
| ModifyContents | `8` | Belgenin içeriğini, tarafından kontrol edilenler dışındaki işlemlerle değiştirinModifyAnnotations ,FillIn , veDocumentAssembly . |
| ModifyAnnotations | `20` | Metin açıklamaları ekleyin veya değiştirin, etkileşimli form alanlarını doldurun veModifyContents is ayrıca etkileşimli form alanlarını (imza alanları dahil) ayarlar, oluşturur veya değiştirir. |
| FillIn | `100` | Mevcut etkileşimli form alanlarını (imza alanları dahil) doldurun.ModifyContents temiz. |
| DocumentAssembly | `400` | Belgeyi birleştirin (sayfaları ekleyin, döndürün veya silin ve belge anahat öğeleri veya thumbnail görüntüleri oluşturun),ModifyContents temiz. |
| Printing | `4` | Belgeyi yazdırın (muhtemelen en yüksek kalite düzeyinde değil, HighResolutionPrintingayrıca ayarlanır). |
| HighResolutionPrinting | `804` | Belgeyi, uygulamaya bağlı bir algoritmaya dayalı olarak, PDF içeriğinin aslına uygun bir dijital kopyasının oluşturulabileceği bir temsile yazdırın. Bu bayrak temizlendiğinde (and Printing ayarlandığında), yazdırma, görünümün düşük düzeyli bir temsili ile sınırlandırılacaktır, muhtemelen düşük kalitede. |

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


