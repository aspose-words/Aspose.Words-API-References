---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts metodu"
linktitle: "get_UseCoreFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts metodu. C++'da TrueType yazı tipleri Arial, Times New Roman, Courier New ve Symbol'ü temel PDF Type 1 yazı tipleriyle değiştirme durumunu belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 32000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


TrueType yazı tipleri Arial, Times New Roman, Courier New ve Symbol'ü temel PDF Type 1 yazı tipleriyle değiştirip değiştirmeyeceğini belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Açıklamalar


Varsayılan değer **false**'dır. Bu değer **true** olarak ayarlandığında, Arial, Times New Roman, Courier New ve Symbol yazı tipleri PDF belgesinde karşılık gelen temel Type 1 yazı tipleriyle değiştirilir.

Temel PDF yazı tipleri, ya da onların yazı tipi ölçümleri ve uygun ikame yazı tipleri, herhangi bir PDF görüntüleyici uygulamasında bulunmalıdır.

Bu ayar yalnızca ANSI (Windows-1252) kodlamasındaki metinler için çalışır. ANSI olmayan metinler, bu ayardan bağımsız olarak gömülü TrueType yazı tipiyle yazılacaktır.

PDF/A ve PDF/UA uyumluluğu tüm yazı tiplerinin gömülmesini gerektirir. PDF/A ve PDF/UA'ya kaydedilirken **false** değeri otomatik olarak kullanılacaktır.

PDF 2.0 formatına kaydedilirken temel yazı tipleri desteklenmez. PDF 2.0'a kaydedilirken **false** değeri otomatik olarak kullanılacaktır.

Bu seçeneğin, [FontEmbeddingMode](../get_fontembeddingmode/) seçeneğine göre daha yüksek önceliği vardır.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
