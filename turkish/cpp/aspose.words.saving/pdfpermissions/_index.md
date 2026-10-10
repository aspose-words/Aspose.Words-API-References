---
title: "Aspose::Words::Saving::PdfPermissions enum"
linktitle: "PdfPermissions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfPermissions enum. C++'ta şifreli bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir."
type: docs
weight: 80000
url: /tr/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Şifreli bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir.

```cpp
enum class PdfPermissions
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| DisallowAll | 0 | PDF belgesindeki tüm işlemleri engeller. Bu varsayılan değerdir. |
| AllowAll | 65535 | PDF belgesindeki tüm işlemlere izin verir. |
| ContentCopy | n/a | Belgeden metin ve grafikleri, [ContentCopyForAccessibility](./) tarafından kontrol edilen işlemler dışındaki işlemlerle kopyalar veya çıkarır. |
| ContentCopyForAccessibility | n/a | Metin ve grafikleri çıkarır (engelli kullanıcıların erişilebilirliğini desteklemek veya başka amaçlar için). |
| ModifyContents | n/a | Belgenin içeriğini, [ModifyAnnotations](./), [FillIn](./) ve [DocumentAssembly](./) tarafından kontrol edilen işlemler dışındaki işlemlerle değiştirir. |
| ModifyAnnotations | n/a | Metin açıklamaları ekler veya değiştirir, etkileşimli form alanlarını doldurur ve [ModifyContents](./) de ayarlanmışsa, etkileşimli form alanlarını (imza alanları dahil) oluşturur veya değiştirir. |
| FillIn | n/a | Mevcut etkileşimli form alanlarını (imza alanları dahil) doldurur, [ModifyContents](./) temiz olsa bile. |
| DocumentAssembly | n/a | Belgeyi birleştirir (sayfaları ekler, döndürür veya siler ve belge taslak öğeleri veya küçük resimler oluşturur), [ModifyContents](./) temiz olsa bile. |
| Printing | n/a | Belgeyi yazdırır (muhtemelen en yüksek kalite seviyesinde olmayabilir, [HighResolutionPrinting](./) de ayarlanmışsa buna bağlıdır). |
| HighResolutionPrinting | n/a | Belgeyi, PDF içeriğinin doğru bir dijital kopyasının oluşturulabileceği bir temsile (uygulamaya bağlı bir algoritma temelinde) yazdırır. Bu bayrak temiz olduğunda (ve [Printing](./) ayarlanmışsa), yazdırma, görünümün düşük seviyeli bir temsiliyle sınırlı olacak ve kalite düşebilir. |

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
