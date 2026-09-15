---
title: "طريقة Aspose::Words::Fonts::FontSettings::get_DefaultInstance"
linktitle: "get_DefaultInstance"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontSettings::get_DefaultInstance. إعدادات الخط الافتراضية الثابتة في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


إعدادات الخط الافتراضية الثابتة.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## أمثلة



يعرض كيفية تكوين كائن إعدادات الخط الافتراضية.
```cpp
// قم بتكوين كائن إعدادات الخط الافتراضية لاستخدام الخط "Courier New"
// كبديل احتياطي عندما نحاول استخدام خط غير معروف.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// هذا المستند لا يحتوي على تكوين FontSettings. عند عرض المستند،
// ستقوم كائن FontSettings الافتراضي بحل الخط المفقود.
// ستستخدم Aspose.Words الخط "Courier New" لعرض النص الذي يستخدم الخط غير المعروف.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## انظر أيضًا

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
