---
title: "Aspose::Words::Fonts::FontFallbackSettings::Save method"
linktitle: "Save"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::Save method. يحفظ إعدادات الاحتياطي الحالية إلى التدفق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.fonts/fontfallbacksettings/save/
---
## FontFallbackSettings::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


يحفظ إعدادات الاحتياطي الحالية إلى التدفق.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإخراج. |

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
## FontFallbackSettings::Save(const System::String\&) method


يحفظ إعدادات الاحتياطي الحالية إلى ملف.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم ملف الإخراج. |

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
## FontFallbackSettings::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Save(std::basic_ostream<CharType, Traits> &outputStream)
```

## انظر أيضًا

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
