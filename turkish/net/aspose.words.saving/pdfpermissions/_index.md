---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: .NET için Aspose.Words
description: Şifrelenmiş PDF'lerde kullanıcı erişimini kontrol etmek için Aspose.Words.PdfPermissions enum'unu keşfedin. Güvenliği artırın ve belge işlemlerini etkili bir şekilde yönetin.
type: docs
weight: 6310
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
| AllowAll | `FFFF` | PDF belgesi üzerinde tüm işlemlere izin verir. |
| ContentCopy | `10` | Belgeden, kontrol edilenden farklı işlemlerle metin ve grafikleri kopyalayın veya başka şekilde çıkarın. ContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Engelli kullanıcıların erişilebilirliğini desteklemek veya diğer amaçlar için metin ve grafikleri ayıklayın. |
| ModifyContents | `8` | Belgenin içeriğini, tarafından kontrol edilenler dışındaki işlemlerle değiştirinModifyAnnotations ,FillIn , VeDocumentAssembly . |
| ModifyAnnotations | `20` | Metin açıklamaları ekleyin veya değiştirin, etkileşimli form alanlarını doldurun ve eğer varsaModifyContents is ayrıca etkileşimli form alanlarını (imza alanları dahil) ayarlar, oluşturur veya değiştirir. |
| FillIn | `100` | İmza alanları dahil olmak üzere mevcut etkileşimli form alanlarını doldurun.ModifyContents açıktır. |
| DocumentAssembly | `400` | Belgeyi birleştirin (sayfaları ekleyin, döndürün veya silin ve belge anahat öğeleri veya küçük resim görüntüleri oluşturun),ModifyContents açıktır. |
| Printing | `4` | Belgeyi yazdırın (en yüksek kalite seviyesinde olmayabilir, buna bağlı olarak)HighResolutionPrinting Ayrıca ayarlanmıştır). |
| HighResolutionPrinting | `804` | Belgeyi, PDF içeriğinin sadık bir dijital kopyasının, uygulamaya bağlı bir algoritmaya dayalı olarak üretilebileceği bir gösterime yazdırın. Bu bayrak temiz olduğunda (ve Printing (ayarlanmıştır), yazdırma, görünümün düşük seviyeli bir gösterimiyle sınırlandırılacaktır, muhtemelen kalitesi bozulmuş. |

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
