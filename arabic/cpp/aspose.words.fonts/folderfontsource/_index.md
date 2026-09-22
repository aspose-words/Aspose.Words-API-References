---
title: "Aspose::Words::Fonts::FolderFontSource class"
linktitle: "FolderFontSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FolderFontSource class. يمثل المجلد الذي يحتوي على ملفات خطوط TrueType. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


يمثل المجلد الذي يحتوي على ملفات خطوط TrueType. لمعرفة المزيد، زر مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | منشئ. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | منشئ. |
| [get_FolderPath](./get_folderpath/)() const | المسار إلى المجلد. |
| [get_Priority](../fontsourcebase/get_priority/)() const | يعيد أولوية مصدر الخط. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | يحدد ما إذا كان يجب مسح المجلدات الفرعية أم لا. |
| [get_Type](./get_type/)() override | يعيد نوع مصدر الخط. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | يعيد قائمة الخطوط المتاحة عبر هذا المصدر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخط.
```cpp
// إنشاء مصدر خط من مجلد يحتوي على ملفات الخطوط.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## انظر أيضًا

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
