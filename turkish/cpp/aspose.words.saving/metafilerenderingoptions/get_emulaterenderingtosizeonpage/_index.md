---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method. C++'da metafile render'ının, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntüleneceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 4334
url: /tr/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Metafile renderlemesinin, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntüleneceğini taklit edip etmeyeceğini belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Açıklamalar


Metafiller MS Word'de görüntülendiğinde, bazı grafikler gerçek metafile boyutuna piksel olarak göre ölçeklenebilir. Yani, yakınlaştırma bile metafile görüntüsünü etkileyebilir.

Bu değer **true** olarak ayarlandığında, Aspose.Words sayfadaki metafile boyutuna göre render etmeyi taklit eder. Piksel cinsinden boyut, sayfadaki metafile boyutundan ve belirtilen [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) değerinden hesaplanır.

Bu değer **false** olarak ayarlandığında, Aspose.Words metafile render'ını piksel cinsinden varsayılan boyutuna göre taklit eder.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer **true**'dır.
## Ayrıca Bakınız

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
