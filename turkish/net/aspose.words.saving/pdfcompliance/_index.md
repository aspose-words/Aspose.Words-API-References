---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: .NET için Aspose.Words
description: PDF standartlarına uyumluluğunuzu artırmak için Aspose.Words.Saving.PdfCompliance enum'unu keşfedin. Her ihtiyaca uygun özelleştirilmiş seçeneklerle belge kalitesini yükseltin!
type: docs
weight: 6200
url: /tr/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

PDF standartlarına uygunluk düzeyini belirtir.

```csharp
public enum PdfCompliance
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Pdf17 | `0` | Çıktı dosyası PDF 1.7 (ISO 32000-1) standardına uygun olacaktır. |
| Pdf20 | `1` | Çıktı dosyası PDF 2.0 (ISO 32000-2) standardına uygun olacaktır. |
| PdfA1a | `2` | Çıktı dosyası PDF/A-1a (ISO 19005-1) standardına uygun olacaktır. Bu seviye PDF/A-1b'nin tüm gereksinimlerini içerir ve ayrıca belgenin yapısının dahil edilmesini (aynı zamanda "etiketlenmesi" olarak da bilinir) gerektirir. Belge içeriğinin aranabilir ve yeniden kullanılabilir olmasını sağlama amacıyla. |
| PdfA1b | `3` | Çıktı dosyası PDF/A-1b (ISO 19005-1) standardına uygun olacaktır. PDF/A-1b'nin amacı, belgenin görsel görünümünün güvenilir bir şekilde yeniden üretilmesini sağlamaktır. |
| PdfA2a | `4` | Çıktı dosyası PDF/A-2a (ISO 19005-2) standardına uygun olacaktır. Bu seviye PDF/A-2u'nun tüm gereksinimlerini içerir ve ayrıca belgenin yapısının dahil edilmesini (aynı zamanda "etiketlenmesi" olarak da bilinir) gerektirir. Belge içeriğinin aranabilir ve yeniden kullanılabilir olmasını sağlama amacıyla. |
| PdfA2u | `5` | Çıktı dosyası PDF/A-2u (ISO 19005-2) standardına uyacaktır. PDF/A-2u, dosyaları oluşturmak, depolamak veya işlemek için kullanılan araçlardan ve sistemlerden bağımsız olarak, belgenin statik görsel görünümünü zaman içinde korumayı hedefler. Ek olarak, belgede bulunan herhangi bir metin bir dizi Unicode kod noktası olarak güvenilir bir şekilde çıkarılabilir. |
| PdfA3a | `6` | Çıktı dosyası PDF/A-3a (ISO 19005-3) standardına uygun olacaktır. Bu seviye PDF/A-3u'nun tüm gereksinimlerini içerir ve ayrıca belgenin yapısının dahil edilmesini (aynı zamanda "etiketlenmesi" olarak da bilinir) gerektirir. Belge içeriğinin aranabilir ve yeniden kullanılabilir olmasını sağlama amacıyla. |
| PdfA3u | `7` | Çıktı dosyası PDF/A-3u (ISO 19005-3) standardına uyacaktır. PDF/A-3u (ve PDF/A-2u), dosyaları oluşturmak, depolamak veya işlemek için kullanılan araçlardan ve sistemlerden bağımsız olarak, zaman içinde belgenin statik görsel görünümünü korumayı hedefler. Ek olarak, belgede bulunan herhangi bir metin bir dizi Unicode kod noktası olarak güvenilir bir şekilde çıkarılabilir. PDF/A-2u'ya ek olarak, PDF/A-3u PDF belgesine eklerin gömülmesine izin verir. |
| PdfA4 | `8` | Çıktı dosyası PDF/A-4 (ISO 19005-4:2020) standardına uyacaktır. PDF/A-4'ün amacı, dosyaları oluşturmak, depolamak veya işlemek için kullanılan araçlardan ve sistemlerden bağımsız olarak, belgenin statik görsel görünümünü zaman içinde korumaktır. Ek olarak, belgede bulunan herhangi bir metin bir dizi Unicode kod noktası olarak güvenilir bir şekilde çıkarılabilir. |
| PdfA4f | `9` | Çıktı dosyası PDF/A-4f (ISO 19005-4:2020) standardına uygun olacaktır. Bu seviye PDF/A-4'ün tüm gereksinimlerini içerir ve ayrıca PDF belgesine eklerin yerleştirilmesine olanak tanır. |
| PdfA4Ua2 | `10` | Çıktı dosyası hem PDF/A-4 (ISO 19005-4:2020) hem de PDF/UA-2 (ISO 14289-2:2024) standartlarına uyacaktır. PDF/A-4, dosyaları oluşturmak, depolamak veya işlemek için kullanılan araçlardan ve sistemlerden bağımsız olarak, belgenin statik görsel görünümünü zaman içinde korumayı hedefler. PDF/UA'nın birincil amacı, elektronik belgelerin PDF formatında dosyanın erişilebilir olmasını sağlayacak şekilde nasıl temsil edileceğini tanımlamaktır. |
| PdfUa1 | `11` | Çıktı dosyası PDF/UA-1 (ISO 14289-1) standardına uygun olacaktır. PDF/UA'nın birincil amacı, elektronik belgelerin PDF formatında dosyanın erişilebilir olmasını sağlayacak şekilde nasıl temsil edileceğini tanımlamaktır. |
| PdfUa2 | `12` | Çıktı dosyası PDF/UA-2 (ISO 14289-2:2024) standardına uygun olacaktır. PDF/UA'nın temel amacı, elektronik belgelerin PDF formatında dosyanın erişilebilir olmasını sağlayacak şekilde nasıl sunulacağını tanımlamaktır. |

## Örnekler

Kaydedilen PDF belgelerinin PDF standartlarına uygunluk düzeyinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
// Standartlardan birine kaydederken bazı PdfSaveOptions'ların yasaklandığını ve otomatik olarak düzeltildiğini unutmayın.
// Hangi seçeneklerin otomatik olarak düzeltildiğini bilmek için IWarningCallback'i kullanın.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "PDF/A-1b" standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfA1b" olarak ayarlayın,
// Aspose.Words'ün PDF'e dönüştürmesiyle belgenin görsel görünümünün korunması amaçlanır.
// "1.7" standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.Pdf17" olarak ayarlayın.
// "PDF/A-1a" standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfA1a" olarak ayarlayın,
// "PDF/A-1b" ile uyumlu olup, orijinal belgenin belge yapısını da korumaktadır.
// "PDF/UA-1" (ISO 14289-1) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfUa1" olarak ayarlayın,
// PDF formatında elektronik dokümanların erişilebilir olmasını sağlayan tanımlamaları amaçlamaktadır.
// "PDF 2.0" (ISO 32000-2) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.Pdf20" olarak ayarlayın.
// "PDF/A-4" (ISO 19004:2020) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfA4" olarak ayarlayın,
// zaman içerisinde belgenin statik görsel görünümünü koruyan.
// Hem PDF/A-4 (ISO 19005-4:2020) hem de PDF/A-4 (ISO 19005-4:2020) ile uyumlu olması için "Uyumluluk" özelliğini "PdfCompliance.PdfA4Ua2" olarak ayarlayın
// ve PDF/UA-2 (ISO 14289-2:2024) standartları.
// PDF/UA-2 (ISO 14289-2:2024) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfUa2" olarak ayarlayın.
// Bu, belgelerin aranabilir olmasına yardımcı olur ancak zaten büyük olan belgelerin boyutunu önemli ölçüde artırabilir.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
