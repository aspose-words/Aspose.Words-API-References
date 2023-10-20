---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Reporting.ReportBuildOptions Sıralama. Davranışını kontrol eden seçenekleri belirtirReportingEngine rapor oluştururken C#'da.
type: docs
weight: 4720
url: /tr/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Davranışını kontrol eden seçenekleri belirtir[`ReportingEngine`](../reportingengine/) rapor oluştururken.

```csharp
[Flags]
public enum ReportBuildOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan seçenekleri belirtir. |
| AllowMissingMembers | `1` | Eksik nesne üyelerinin motor tarafından boş değişmez değerler olarak değerlendirilmesi gerektiğini belirtir. Bu seçeneği yalnızca örnek (yani statik olmayan) nesne üyelerine ve uzantı yöntemlerine erişimi etkiler. Bu seçeneği ayarlanmazsa, motor eksik bir nesne üyesiyle karşılaştığında bir istisna oluşturur. |
| RemoveEmptyParagraphs | `2` | Şablon sözdizimi etiketleri kaldırıldıktan veya boş değerlerle değiştirildikten sonra motorun boş hale gelen paragrafları kaldırması gerektiğini belirtir. |
| InlineErrorMessages | `4` | Motorun şablon sözdizimi hata mesajlarını çıktı belgelerine satır içi olarak koyması gerektiğini belirtir. Bu seçenek ayarlanmazsa, motor bir sözdizimi hatasıyla karşılaştığında bir istisna oluşturur. |
| UseLegacyHeaderFooterVisiting | `8` | Motorun, Aspose.Words 21.9. öncesi sürümleriyle uyumlu bir order içindeki bölüm alt düğümlerini (üstbilgiler, altbilgiler, gövdeler) ziyaret etmesi gerektiğini belirtir. |
| RespectJpegExifOrientation | `10` | Motorun, eklenen JPEG görüntülerini uygun şekilde döndürmek için EXIF ​​görüntü yönlendirme değerlerini kullanması gerektiğini belirtir. |

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
