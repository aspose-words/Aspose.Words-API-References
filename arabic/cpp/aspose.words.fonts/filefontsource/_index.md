---
title: "الفئة Aspose::Words::Fonts::FileFontSource"
linktitle: "FileFontSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::Fonts::FileFontSource. تمثل ملف خط TrueType واحد مخزن في نظام الملفات. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


يمثل ملف الخط TrueType الفردي المخزن في نظام الملفات. لمعرفة المزيد، زر مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | منشئ. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | منشئ. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | منشئ. |
| [get_CacheKey](./get_cachekey/)() const | المفتاح لهذا المصدر في الذاكرة المؤقتة. |
| [get_FilePath](./get_filepath/)() const | المسار إلى ملف الخط. |
| [get_Priority](../fontsourcebase/get_priority/)() const | يعيد أولوية مصدر الخط. |
| [get_Type](./get_type/)() override | يعيد نوع مصدر الخط. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | يعيد قائمة الخطوط المتاحة عبر هذا المصدر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية استخدام ملف خط في نظام الملفات المحلي كمصدر للخط.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## انظر أيضًا

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
