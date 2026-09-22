---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. C++'da ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak dış veri kaynağının türünü belirtir."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


ODSO bağlantı bilgilerinin bir parçası olarak bağlanılacak harici veri kaynağının türünü belirtir.

```cpp
enum class OdsoDataSourceType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Metin | 0 | Belirtilen belgenin bir metin dosyasına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOther. |
| Database | 1 | Belirtilen belgenin bir veritabanına bağlandığını belirtir. Muhtemelen wdMergeSubTypeAccess. |
| AdresDefteri | 2 | Belirli bir belgenin bir kişi adres defterine bağlandığını belirtir. Muhtemelen wdMergeSubTypeOAL. |
| Belge1 | 3 | Belirli bir belgenin, üretici uygulama tarafından desteklenen başka bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOLEDBWord. |
| Belge2 | 4 | Belirli bir belgenin, üretici uygulama tarafından desteklenen başka bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeWorks. |
| Native | 5 | Belirli bir belgenin, üretici uygulamaya özgü başka bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOLEDBText. |
| Email | 6 | Belirli bir belgenin bir e-posta uygulamasına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOutlook. |
| None | 7 | Harici veri kaynağının türü belirtilmemiştir. Muhtemelen wdMergeSubTypeWord. |
| Eski | 8 | Belirli bir belgenin, üretici uygulama tarafından desteklenen eski bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeWord2000. |
| Ana | 9 | Belirli bir belgenin, diğer veri kaynaklarını toplayan bir veri kaynağına bağlandığını belirtir. |
| Default | n/a | Şuna eşittir [None](./). |

## Açıklamalar


OOXML spesifikasyonu bu enum için çok belirsizdir. Sanırım WdMergeSubType enumına karşılık geliyor [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
