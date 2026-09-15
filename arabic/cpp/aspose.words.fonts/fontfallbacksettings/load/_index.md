---
title: "طريقة Aspose::Words::Fonts::FontFallbackSettings::Load"
linktitle: "Load"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontFallbackSettings::Load. تقوم بتحميل إعدادات الاحتياطي من تدفق XML في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fonts/fontfallbacksettings/load/
---
## FontFallbackSettings::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


يقوم بتحميل إعدادات الاحتياطي من تدفق XML.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإدخال. |

## أمثلة



يظهر كيفية تحميل وحفظ إعدادات الاحتياطي للخط من/إلى تدفق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// حمّل مستند XML يحدد مجموعة من إعدادات الاحتياطي للخط.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// استخدم تدفقًا لحفظ إعدادات الاحتياطي الحالية للخط في مستند XML.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## انظر أيضًا

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(const System::String\&) method


يقوم بتحميل إعدادات احتياطي الخط من ملف XML.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم ملف الإدخال. |

## أمثلة



يظهر كيفية تحميل وحفظ إعدادات الاحتياطي للخط من/إلى مستند XML في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// حمّل مستند XML يحدد مجموعة من إعدادات الاحتياطي للخط.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_FallbackSettings()->Load(get_MyDir() + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// احفظ إعدادات الاحتياطي الحالية للخط في مستند XML.
doc->get_FontSettings()->get_FallbackSettings()->Save(get_ArtifactsDir() + u"FallbackSettings.xml");
```

## انظر أيضًا

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Load(std::basic_istream<CharType, Traits> &stream)
```

## انظر أيضًا

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
