---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::StreamFontSource sınıfı. Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıftır. Daha fazla bilgi için C++'daki  dokümantasyon makalesini ziyaret edin."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıftır. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Bu kaynağın önbellekteki anahtarı. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Yazı tipi kaynağı önceliğini döndürür. |
| [get_Type](./get_type/)() override | Yazı tipi kaynağının türünü döndürür. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Bu yöntem, gerektiğinde yazı tipi verileriyle akışı açmalıdır. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| static [Type](./type/)() |  |
## Açıklamalar


Akış yazı tipi kaynağını kullanmak için, [StreamFontSource](./) sınıfından türetilmiş bir sınıf oluşturmalı ve [OpenFontDataStream](./openfontdatastream/) yönteminin uygulanmasını sağlamalısınız.

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## Ayrıca Bakınız

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
