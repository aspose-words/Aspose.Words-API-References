---
title: "فئة Aspose::Words::Fonts::MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::MemoryFontSource. تمثل ملف خط TrueType واحد مخزن في الذاكرة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


يمثل ملف TrueType الخط الفردي المخزن في الذاكرة. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | المفتاح لهذا المصدر في الذاكرة المؤقتة. |
| [get_FontData](./get_fontdata/)() const | بيانات الخط الثنائية. |
| [get_Priority](../fontsourcebase/get_priority/)() const | يعيد أولوية مصدر الخط. |
| [get_Type](./get_type/)() override | يعيد نوع مصدر الخط. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | يعيد قائمة الخطوط المتاحة عبر هذا المصدر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | منشئ. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | منشئ. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | منشئ. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## انظر أيضًا

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
