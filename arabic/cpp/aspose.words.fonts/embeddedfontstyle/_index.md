---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. يحدد نمط الخط المضمن داخل كائن FontInfo في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


يحدد نمط الخط المضمن داخل كائن [FontInfo](../fontinfo/).

```cpp
enum class EmbeddedFontStyle
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Regular | 0 | يحدد الخط المدمج العادي. |
| عريض | 1 | يحدد الخط المدمج العريض. |
| مائل | 2 | يحدد الخط المدمج المائل. |
| عريض مائل | 3 | يحدد الخط المدمج العريض-المائل. |


## أمثلة



يوضح كيفية استخراج خط مدمج من مستند، وحفظه على نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// قد تكون صيغ الخطوط المدمجة مختلفة في صيغ أخرى مثل .doc.
// نحتاج إلى معرفة الصيغة الصحيحة قبل أن نتمكن من استخراج الخط.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// كما يمكننا تحويل صيغة OpenType المدمجة، التي تأتي من مستندات .doc، إلى OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## انظر أيضًا

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
