---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts yöntemi"
linktitle: "get_EmbedFullFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts yöntemi. C++'de oluşturulan PDF belgelerine yazı tiplerinin nasıl gömüleceğini kontrol eder."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Yazı tiplerinin ortaya çıkan PDF belgelerine nasıl gömüleceğini kontrol eder.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Açıklamalar


Varsayılan değer **false**'tur, bu da yazı tiplerinin gömülmeden önce alt kümeleme yapıldığı anlamına gelir. Alt kümeleme, çıktı dosya boyutunu daha küçük tutmak istediğinizde faydalıdır. Alt kümeleme, bir yazı tipindeki kullanılmayan tüm glifleri kaldırır.

Bu değer **true** olarak ayarlandığında, tam bir yazı tipi dosyası alt kümeleme yapılmadan PDF'ye gömülür. Bu, daha büyük çıktı dosyalarına neden olur, ancak oluşturulan PDF'yi daha sonra düzenlemek istediğinizde (ör. daha fazla metin eklemek) yararlı bir seçenek olabilir.

Bazı yazı tipleri büyüktür (birkaç megabayt) ve onları alt kümeleme yapmadan gömmek büyük çıktı belgelerine yol açar.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
