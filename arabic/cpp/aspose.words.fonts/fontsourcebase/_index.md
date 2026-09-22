---
title: "فئة Aspose::Words::Fonts::FontSourceBase"
linktitle: "FontSourceBase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::FontSourceBase. هذه فئة أساسية مجردة للفئات التي تسمح للمستخدم بتحديد مصادر خطوط مختلفة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


هذه فئة أساسية مجردة للفئات التي تسمح للمستخدم بتحديد مصادر خطوط مختلفة. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Priority](./get_priority/)() const | يعيد أولوية مصدر الخط. |
| virtual [get_Type](./get_type/)() | يعيد نوع مصدر الخط. |
| [get_WarningCallback](./get_warningcallback/)() const | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [GetAvailableFonts](./getavailablefonts/)() | يعيد قائمة الخطوط المتاحة عبر هذا المصدر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
