---
title: Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat method
linktitle: ContentTypeToSaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat method. Converts IANA content type into a save format enumerated value in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil::ContentTypeToSaveFormat method


Converts IANA content type into a save format enumerated value.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(const System::String & contentType)
```

## Examples


Shows how to find the corresponding Aspose load/save format from each media type string.

```cpp
// The ContentTypeToSaveFormat/ContentTypeToLoadFormat methods only accept official IANA media type names, also known as MIME types.
// All valid media types are listed here: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Trying to associate a SaveFormat with a partial media type string will not work.
ASSERT_THROW(System::Action<>(static_cast<std::function<void()>>([]() -> void
{
    FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
}))(), System::ArgumentException);

// If Aspose.Words does not have a corresponding save/load format for a content type, an exception will also be thrown.
ASSERT_THROW(System::Action<>(static_cast<std::function<void()>>([]() -> void
{
    FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
}))(), System::ArgumentException);

// Files of the types listed below can be saved, but not loaded using Aspose.Words.
ASSERT_THROW(System::Action<>(static_cast<std::function<void()>>([]() -> void
{
    FileFormatUtil::ContentTypeToLoadFormat(u"image/jpeg");
}))(), System::ArgumentException);

ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"image/jpeg"), SaveFormat::Jpeg);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"image/png"), SaveFormat::Png);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"image/tiff"), SaveFormat::Tiff);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"image/gif"), SaveFormat::Gif);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"image/x-emf"), SaveFormat::Emf);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.ms-xpsdocument"), SaveFormat::Xps);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"application/pdf"), SaveFormat::Pdf);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"image/svg+xml"), SaveFormat::Svg);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"application/epub+zip"), SaveFormat::Epub);

// For file types that can be saved and loaded, we can match a media type to both a load format and a save format.
ASSERT_EQ(FileFormatUtil::ContentTypeToLoadFormat(u"application/msword"), LoadFormat::Doc);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"application/msword"), SaveFormat::Doc);

ASSERT_EQ(FileFormatUtil::ContentTypeToLoadFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"), LoadFormat::Docx);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"), SaveFormat::Docx);

ASSERT_EQ(FileFormatUtil::ContentTypeToLoadFormat(u"text/plain"), LoadFormat::Text);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"text/plain"), SaveFormat::Text);

ASSERT_EQ(FileFormatUtil::ContentTypeToLoadFormat(u"application/rtf"), LoadFormat::Rtf);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"application/rtf"), SaveFormat::Rtf);

ASSERT_EQ(FileFormatUtil::ContentTypeToLoadFormat(u"text/html"), LoadFormat::Html);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"text/html"), SaveFormat::Html);

ASSERT_EQ(FileFormatUtil::ContentTypeToLoadFormat(u"multipart/related"), LoadFormat::Mhtml);
ASSERT_EQ(FileFormatUtil::ContentTypeToSaveFormat(u"multipart/related"), SaveFormat::Mhtml);
```
## Exceptions

* ArgumentException - Throws when cannot convert.

## See Also

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
