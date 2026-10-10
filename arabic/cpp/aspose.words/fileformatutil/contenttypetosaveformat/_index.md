---
title: "طريقة Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat"
linktitle: "ContentTypeToSaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat. تقوم بتحويل نوع المحتوى IANA إلى قيمة تنسيق حفظ مُعدَّة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil::ContentTypeToSaveFormat method


يحوّل نوع محتوى IANA إلى قيمة تعداد صيغة الحفظ.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(const System::String &contentType)
```


## أمثلة



يوضح كيفية العثور على تنسيق التحميل/الحفظ المقابل لـ **Aspose** من كل سلسلة نوع وسائط.
```cpp
// تقبل طرق ContentTypeToSaveFormat/ContentTypeToLoadFormat فقط أسماء أنواع وسائط IANA الرسمية، المعروفة أيضًا باسم أنواع MIME.
// جميع أنواع الوسائط الصالحة مدرجة هنا: https://www.iana.org/assignments/media-types/media-types.xhtml.

// محاولة ربط SaveFormat بسلسلة نوع وسائط جزئية لن تنجح.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
})(), System::ArgumentException);

// إذا لم يكن لدى Aspose.Words تنسيق حفظ/تحميل مطابق لنوع المحتوى، سيتم أيضًا رمي استثناء.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
})(), System::ArgumentException);

// يمكن حفظ الملفات من الأنواع المذكورة أدناه، ولكن لا يمكن تحميلها باستخدام Aspose.Words.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"image/jpeg");
})(), System::ArgumentException);

ASSERT_EQ(Aspose::Words::SaveFormat::Jpeg, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"image/jpeg"));
ASSERT_EQ(Aspose::Words::SaveFormat::Png, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"image/png"));
ASSERT_EQ(Aspose::Words::SaveFormat::Tiff, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"image/tiff"));
ASSERT_EQ(Aspose::Words::SaveFormat::Gif, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"image/gif"));
ASSERT_EQ(Aspose::Words::SaveFormat::Emf, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"image/x-emf"));
ASSERT_EQ(Aspose::Words::SaveFormat::Xps, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.ms-xpsdocument"));
ASSERT_EQ(Aspose::Words::SaveFormat::Pdf, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/pdf"));
ASSERT_EQ(Aspose::Words::SaveFormat::Svg, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"image/svg+xml"));
ASSERT_EQ(Aspose::Words::SaveFormat::Epub, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/epub+zip"));

// بالنسبة لأنواع الملفات التي يمكن حفظها وتحميلها، يمكننا مطابقة نوع الوسائط مع كل من تنسيق التحميل وتنسيق الحفظ.
ASSERT_EQ(Aspose::Words::LoadFormat::Doc, Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"application/msword"));
ASSERT_EQ(Aspose::Words::SaveFormat::Doc, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/msword"));

ASSERT_EQ(Aspose::Words::LoadFormat::Docx, Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
ASSERT_EQ(Aspose::Words::SaveFormat::Docx, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

ASSERT_EQ(Aspose::Words::LoadFormat::Text, Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"text/plain"));
ASSERT_EQ(Aspose::Words::SaveFormat::Text, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"text/plain"));

ASSERT_EQ(Aspose::Words::LoadFormat::Rtf, Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"application/rtf"));
ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/rtf"));

ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"text/html"));
ASSERT_EQ(Aspose::Words::SaveFormat::Html, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"text/html"));

ASSERT_EQ(Aspose::Words::LoadFormat::Mhtml, Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(u"multipart/related"));
ASSERT_EQ(Aspose::Words::SaveFormat::Mhtml, Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"multipart/related"));
```

## انظر أيضًا

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
