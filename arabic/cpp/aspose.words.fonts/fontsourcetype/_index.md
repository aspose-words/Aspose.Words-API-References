---
title: "Aspose::Words::Fonts::FontSourceType تعداد"
linktitle: "FontSourceType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontSourceType enum. يحدد نوع مصدر الخط في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


يحدد نوع مصدر الخط.

```cpp
enum class FontSourceType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| FontFile | 0 | كائن [FileFontSource](../filefontsource/) يمثل ملف خط واحد. |
| FontsFolder | 1 | كائن [FolderFontSource](../folderfontsource/) يمثل مجلدًا يحتوي على ملفات الخطوط. |
| MemoryFont | 2 | كائن [MemoryFontSource](../memoryfontsource/) يمثل خطًا واحدًا في الذاكرة. |
| SystemFonts | 3 | كائن [SystemFontSource](../systemfontsource/) يمثل جميع الخطوط المثبتة على النظام. |
| FontStream | 4 | كائن [StreamFontSource](../streamfontsource/) يمثل تدفقًا يحتوي على بيانات الخط. |


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
