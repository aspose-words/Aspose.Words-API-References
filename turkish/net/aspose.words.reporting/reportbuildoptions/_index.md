---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: .NET için Aspose.Words
description: Verimli rapor oluşturma için Aspose.Words ReportingEngine seçeneklerini keşfedin. En iyi sonuçlar için esnek ayarlarla raporlamanızı özelleştirin.
type: docs
weight: 5460
url: /tr/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Davranışı kontrol eden seçenekleri belirtir[`ReportingEngine`](../reportingengine/) bir rapor oluştururken.

```csharp
[Flags]
public enum ReportBuildOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan seçenekleri belirtir. |
| AllowMissingMembers | `1` | Eksik nesne üyelerinin motor tarafından boş sabitler olarak ele alınması gerektiğini belirtir. Bu seçenek yalnızca örnek (yani statik olmayan) nesne üyelerine ve uzantı yöntemlerine erişimi etkiler. Bu seçeneği ayarlanmamışsa, motor eksik bir nesne üyesiyle karşılaştığında bir istisna atar. |
| RemoveEmptyParagraphs | `2` | Şablon sözdizimi etiketleri kaldırıldıktan veya boş değerlerle değiştirildikten sonra motorun boş olan paragrafları kaldırması gerektiğini belirtir. |
| InlineErrorMessages | `4` | Motorun şablon sözdizimi hata iletilerini çıktı belgelerine satır içi olarak eklemesi gerektiğini belirtir. Bu seçenek ayarlanmazsa, motor bir sözdizimi hatasıyla karşılaştığında bir istisna atar. |
| UseLegacyHeaderFooterVisiting | `8` | Motorun bölüm alt düğümlerini (başlıklar, altbilgiler, gövdeler) bir sırayla ziyaret etmesi gerektiğini belirtir. Aspose.Words'ün 21.9'dan önceki sürümleriyle uyumludur. |
| RespectJpegExifOrientation | `10` | Motorun eklenen JPEG resimlerini uygun şekilde döndürmek için EXIF ​​​​resim yönlendirme değerlerini kullanması gerektiğini belirtir. |
| UpdateFieldsSyntaxAware | `20` | Motorun alan sonuçlarındaki şablon sözdizimini yoksayması ve bir rapor oluşturulduktan sonra alanları güncellemesi gerektiğini belirtir. |

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
