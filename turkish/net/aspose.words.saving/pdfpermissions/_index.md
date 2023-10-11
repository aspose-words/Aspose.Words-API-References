---
title: Enum PdfPermissions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfPermissions Sıralama. Şifrelenmiş bir PDF belgesinde kullanıcıya izin verilen işlemleri belirtir.
type: docs
weight: 5510
url: /tr/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Şifrelenmiş bir PDF belgesinde kullanıcıya izin verilen işlemleri belirtir.

```csharp
[Flags]
public enum PdfPermissions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| DisallowAll | `0` | PDF belgesindeki tüm işlemlere izin vermez. Bu varsayılan değerdir. |
| AllowAll | `FFFF` | PDF belgesi üzerinde tüm işlemlere izin verir. |
| ContentCopy | `10` | Belgeden metin ve grafikleri, kontrol edilen dışındaki işlemlerle kopyalayın veya başka şekilde çıkarınContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Metin ve grafikleri çıkarın (engelli kullanıcıların erişimini desteklemek amacıyla veya başka amaçlarla). |
| ModifyContents | `8` | Belgenin içeriğini, tarafından kontrol edilenler dışındaki işlemlerle değiştirinModifyAnnotations ,FillIn , VeDocumentAssembly . |
| ModifyAnnotations | `20` | Metin açıklamalarını ekleyin veya değiştirin, etkileşimli form alanlarını doldurun ve gerekiyorsaModifyContents is ayrıca etkileşimli form alanlarını (imza alanları dahil) ayarlar, oluşturur veya değiştirir. |
| FillIn | `100` | Mevcut etkileşimli form alanlarını (imza alanları dahil) doldurun.ModifyContents temiz. |
| DocumentAssembly | `400` | Belgeyi birleştirin (sayfaları ekleyin, döndürün veya silin ve belge anahat öğeleri veya küçük resim görüntüleri oluşturun), hattaModifyContents açık. |
| Printing | `4` | Belgeyi yazdırın ( olup olmadığına bağlı olarak muhtemelen en yüksek kalite düzeyinde değil)HighResolutionPrinting ayrıca ayarlanmıştır). |
| HighResolutionPrinting | `804` | Belgeyi, uygulamaya bağlı bir algoritmaya dayalı olarak PDF içeriğinin aslına sadık bir dijital kopyasının oluşturulabileceği bir temsile yazdırın. Bu bayrak temiz olduğunda (and Printing ayarlandığında), yazdırma, görünümün düşük seviyeli temsiliyle sınırlı olacaktır, muhtemelen kalitesi düşmüş. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


