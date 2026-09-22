---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode yöntemi"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode yöntemi. EMF+ Dual metafile'ların C++'da nasıl render edileceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


EMF+ Dual metafile'lerin nasıl render edileceğini belirleyen bir değeri alır veya ayarlar.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Açıklamalar


EMF+ Dual metafile'lar hem EMF+ hem de EMF bölümlerini içerir. MS Word ve GDI+ her zaman EMF+ bölümünü render eder. Aspose.Words şu anda tüm EMF+ kayıtlarını tam olarak desteklememekte ve bazı durumlarda EMF bölümünün render sonucu EMF+ bölümünün sonucundan daha iyi görünmektedir.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır. Metafile bitmap'e render edildiğinde ise EMF+ bölümü her zaman kullanılır.

Varsayılan değer [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## Ayrıca Bakınız

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
