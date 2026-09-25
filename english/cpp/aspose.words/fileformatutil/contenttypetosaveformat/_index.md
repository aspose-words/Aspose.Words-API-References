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
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(const System::String &contentType)
```


## Examples



Shows how to find the corresponding **Aspose** load/save format from each media type string. 
```cpp
// The ContentTypeToSaveFormat/ContentTypeToLoadFormat methods only accept official IANA media type names, also known as MIME types.
// All valid media types are listed here: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Trying to associate a SaveFormat with a partial media type string will not work.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
})(), System::ArgumentException);

// If Aspose.Words does not have a corresponding save/load format for a content type, an exception will also be thrown.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
})(), System::ArgumentException);

// Files of the types listed below can be saved, but not loaded using Aspose.Words.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    FileFormatUtil::ContentTypeToLoadFormat(u"image/jpeg");
})(), System::ArgumentException);

ASSERT_EQ(Aspose::Words::SaveFormat::Jpeg, FileFormatUtil::ContentTypeToSaveFormat(u"image/jpeg"));
ASSERT_EQ(Aspose::Words::SaveFormat::Png, FileFormatUtil::ContentTypeToSaveFormat(u"image/png"));
ASSERT_EQ(Aspose::Words::SaveFormat::Tiff, FileFormatUtil::ContentTypeToSaveFormat(u"image/tiff"));
ASSERT_EQ(Aspose::Words::SaveFormat::Gif, FileFormatUtil::ContentTypeToSaveFormat(u"image/gif"));
ASSERT_EQ(Aspose::Words::SaveFormat::Emf, FileFormatUtil::ContentTypeToSaveFormat(u"image/x-emf"));
ASSERT_EQ(Aspose::Words::SaveFormat::Xps, FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.ms-xpsdocument"));
ASSERT_EQ(Aspose::Words::SaveFormat::Pdf, FileFormatUtil::ContentTypeToSaveFormat(u"application/pdf"));
ASSERT_EQ(Aspose::Words::SaveFormat::Svg, FileFormatUtil::ContentTypeToSaveFormat(u"image/svg+xml"));
ASSERT_EQ(Aspose::Words::SaveFormat::Epub, FileFormatUtil::ContentTypeToSaveFormat(u"application/epub+zip"));

// For file types that can be saved and loaded, we can match a media type to both a load format and a save format.
ASSERT_EQ(Aspose::Words::LoadFormat::Doc, FileFormatUtil::ContentTypeToLoadFormat(u"application/msword"));
ASSERT_EQ(Aspose::Words::SaveFormat::Doc, FileFormatUtil::ContentTypeToSaveFormat(u"application/msword"));

ASSERT_EQ(Aspose::Words::LoadFormat::Docx, FileFormatUtil::ContentTypeToLoadFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
ASSERT_EQ(Aspose::Words::SaveFormat::Docx, FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

ASSERT_EQ(Aspose::Words::LoadFormat::Text, FileFormatUtil::ContentTypeToLoadFormat(u"text/plain"));
ASSERT_EQ(Aspose::Words::SaveFormat::Text, FileFormatUtil::ContentTypeToSaveFormat(u"text/plain"));

ASSERT_EQ(Aspose::Words::LoadFormat::Rtf, FileFormatUtil::ContentTypeToLoadFormat(u"application/rtf"));
ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, FileFormatUtil::ContentTypeToSaveFormat(u"application/rtf"));

ASSERT_EQ(Aspose::Words::LoadFormat::Html, FileFormatUtil::ContentTypeToLoadFormat(u"text/html"));
ASSERT_EQ(Aspose::Words::SaveFormat::Html, FileFormatUtil::ContentTypeToSaveFormat(u"text/html"));

ASSERT_EQ(Aspose::Words::LoadFormat::Mhtml, FileFormatUtil::ContentTypeToLoadFormat(u"multipart/related"));
ASSERT_EQ(Aspose::Words::SaveFormat::Mhtml, FileFormatUtil::ContentTypeToSaveFormat(u"multipart/related"));
```

## See Also

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
