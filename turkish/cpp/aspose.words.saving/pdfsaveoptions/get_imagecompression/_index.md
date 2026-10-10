---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression yöntemi"
linktitle: "get_ImageCompression"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression yöntemi. C++'ta belgede bulunan tüm görüntüler için kullanılacak sıkıştırma türünü belirtir."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Belgedeki tüm görüntüler için kullanılacak sıkıştırma türünü belirtir.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Açıklamalar


Varsayılan [Auto](../../pdfimagecompression/)'dır.

[Jpeg](../../pdfimagecompression/) kullanarak, çıktıda yer alan görüntülerin kalitesini [JpegQuality](../get_jpegquality/) özelliği aracılığıyla kontrol edebilirsiniz.

[Jpeg](../../pdfimagecompression/) kullanmak, diğer sıkıştırma türleriyle karşılaştırıldığında en hızlı dönüşüm hızını sağlar, ancak bu durumda kayıplı JPEG sıkıştırması uygulanır.

[Auto](../../pdfimagecompression/) kullanarak, çıktıda Jpeg kalitesini [JpegQuality](../get_jpegquality/) özelliğiyle kontrol edebilirsiniz; ancak diğer formatlar için ham piksel verileri çıkarılır ve Flate sıkıştırmasıyla kaydedilir. Bu durum Jpeg dönüşümünden daha yavaştır ancak kayıpsızdır.
## Ayrıca Bakınız

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
