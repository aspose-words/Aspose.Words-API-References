---
title: "الفئة Aspose::Words::Fonts::StreamFontSource"
linktitle: "StreamFontSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::Fonts::StreamFontSource. الفئة الأساسية لمصدر خط تدفق معرف من قبل المستخدم. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


الفئة الأساسية لمصدر خط تدفق معرف من قبل المستخدم. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | المفتاح لهذا المصدر في الذاكرة المؤقتة. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | يعيد أولوية مصدر الخط. |
| [get_Type](./get_type/)() override | يعيد نوع مصدر الخط. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | يعيد قائمة الخطوط المتاحة عبر هذا المصدر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | يجب أن تفتح هذه الطريقة التدفق ببيانات الخط عند الطلب. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| static [Type](./type/)() |  |
## ملاحظات


من أجل استخدام مصدر خط التدفق، يجب عليك إنشاء فئة مشتقة من [StreamFontSource](./) وتوفير تنفيذ طريقة [OpenFontDataStream](./openfontdatastream/).

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## انظر أيضًا

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
