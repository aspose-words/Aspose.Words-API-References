---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method"
linktitle: "get_EmulateRasterOperations"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method. C++'da raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Açıklamalar


Metafilllerde belirli raster işlemleri kullanılabilir. Bunlar doğrudan vektör grafik olarak render edilemez. Raster işlemlerinin taklit edilmesi, ortaya çıkan vektör grafiğin kısmi rasterleştirilmesini gerektirir ve bu, metafile render performansını etkileyebilir.

Bu değer **true** olarak ayarlandığında, Aspose.Words raster işlemlerini taklit eder. Oluşan çıktı kısmen rasterleştirilebilir ve performans daha yavaş olabilir.

Bu değer **false** olarak ayarlandığında, Aspose.Words raster işlemlerini taklit etmez. [Aspose.Words](../../../aspose.words/) bir metafilde raster işlemiyle karşılaştığında, işletim sistemini kullanarak metafili bitmap olarak render etmeye geri döner.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer **true**'dır.
## Ayrıca Bakınız

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
