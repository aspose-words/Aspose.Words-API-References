---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf yöntemi"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf yöntemi. Gömülü EMF metafile'lı WMF metafile'ların C++'da nasıl render edileceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Gömülü EMF metafile'li WMF metafile'lerin nasıl render edileceğini belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Açıklamalar


WMF metafile'ları gömülü EMF verisi içerebilir. MS Word çoğu durumda gömülü EMF verisini kullanır. GDI+ her zaman WMF verisini kullanır.

Bu değer **true** olarak ayarlandığında, Aspose.Words render ederken gömülü EMF verisini kullanır.

Bu değer **false** olarak ayarlandığında, Aspose.Words render ederken WMF verisini kullanır.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır. Metafile bitmap olarak render edildiğinde ise WMF verisi her zaman kullanılır.

Varsayılan değer **true**'dır.
## Ayrıca Bakınız

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
