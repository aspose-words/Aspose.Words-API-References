---
title: "Aspose::Words::Fonts::FontSourceBase::get_Type طريقة"
linktitle: "get_Type"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontSourceBase::get_Type طريقة. تُرجع نوع مصدر الخط في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fonts/fontsourcebase/get_type/
---
## FontSourceBase::get_Type method


يعيد نوع مصدر الخط.

```cpp
virtual Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FontSourceBase::get_Type()=0
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
