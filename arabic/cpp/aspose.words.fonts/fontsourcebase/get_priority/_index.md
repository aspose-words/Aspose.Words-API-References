---
title: "طريقة get_Priority في Aspose::Words::Fonts::FontSourceBase"
linktitle: "get_Priority"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة get_Priority في Aspose::Words::Fonts::FontSourceBase. تُرجع أولوية مصدر الخط في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


يعيد أولوية مصدر الخط.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## ملاحظات


هذه القيمة تُستخدم عندما تكون هناك خطوط بنفس اسم العائلة والنمط في مصادر خطوط مختلفة. في هذه الحالة، تختار Aspose.Words الخط من المصدر الذي له قيمة أولوية أعلى.

القيمة الافتراضية هي 0.

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

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
