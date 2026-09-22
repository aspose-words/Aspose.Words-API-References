---
title: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality metodu"
linktitle: "get_JpegQuality"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality metodu. JPEG görüntülerinin PDF belgesi içindeki kalitesini belirleyen bir değeri alır veya ayarlar C++'da."
type: docs
weight: 23000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


PDF belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Açıklamalar


Varsayılan değer 100'tür.

Bu özellik, [ImageCompression](../get_imagecompression/) seçeneği ile birlikte kullanılır.

Yalnızca bir belge JPEG görüntüleri içerdiğinde etkili olur.

Bu özelliği, PDF formatında kaydederken bir belgedeki görüntülerin kalitesini alıp ayarlamak için kullanın. Değer 0 ile 100 arasında değişebilir; 0 en düşük kaliteyi ancak en yüksek sıkıştırmayı, 100 ise en yüksek kaliteyi ancak en düşük sıkıştırmayı ifade eder. Kalite 100 ve kaynak görüntü JPEG ise, sıkıştırma yok demektir - orijinal baytlar kaydedilir.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
