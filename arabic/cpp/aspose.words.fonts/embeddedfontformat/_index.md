---
title: "تعداد Aspose::Words::Fonts::EmbeddedFontFormat enum"
linktitle: "EmbeddedFontFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Fonts::EmbeddedFontFormat. يحدد تنسيق الخط المضمّن المحدد داخل كائن FontInfo. عند حفظ المستند إلى ملف، يتم كتابة الخطوط المضمّنة ذات التنسيق المطابق فقط في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


يحدد تنسيق الخط المضمّن المحدد داخل كائن [معلومات الخط](../fontinfo/) . عند حفظ المستند إلى ملف، يتم كتابة الخطوط المضمّنة ذات التنسيق المطابق فقط.

```cpp
enum class EmbeddedFontFormat
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| EmbeddedOpenType | 0 | يحدد تنسيق ملف Embedded OpenType (EOT). يُستخدم هذا التنسيق للخطوط المضمّنة في ملفات DOC. |
| OpenType | 1 | يحدد الخط المضمّن كنسخة عادية من ملف خط OpenType (TrueType). يُستخدم هذا التنسيق للخطوط المضمّنة في تنسيق Open Office XML، بما في ذلك ملفات DOCX. |


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
