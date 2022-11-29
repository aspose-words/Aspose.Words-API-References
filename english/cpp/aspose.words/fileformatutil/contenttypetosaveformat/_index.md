---
title: ContentTypeToSaveFormat
second_title: Aspose.Words for C++ API Reference
description: Converts IANA content type into a save format enumerated value.
type: docs
weight: 14
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
ASSERT_THROW(FileFormatUtil::ContentTypeToSaveFormat(u"jpeg"), System::ArgumentException);

// If Aspose.Words does not have a corresponding save/load format for a content type, an exception will also be thrown.
ASSERT_THROW(FileFormatUtil::ContentTypeToSaveFormat(u"application/zip"), System::ArgumentException);

// Files of the types listed below can be saved, but not loaded using Aspose.Words.
ASSERT_THROW(FileFormatUtil::ContentTypeToLoadFormat(u"image/jpeg"), System::ArgumentException);

ASSERT_EQ(SaveFormat::Jpeg, FileFormatUtil::ContentTypeToSaveFormat(u"image/jpeg"));
ASSERT_EQ(SaveFormat::Png, FileFormatUtil::ContentTypeToSaveFormat(u"image/png"));
ASSERT_EQ(SaveFormat::Tiff, FileFormatUtil::ContentTypeToSaveFormat(u"image/tiff"));
ASSERT_EQ(SaveFormat::Gif, FileFormatUtil::ContentTypeToSaveFormat(u"image/gif"));
ASSERT_EQ(SaveFormat::Emf, FileFormatUtil::ContentTypeToSaveFormat(u"image/x-emf"));
ASSERT_EQ(SaveFormat::Xps, FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.ms-xpsdocument"));
ASSERT_EQ(SaveFormat::Pdf, FileFormatUtil::ContentTypeToSaveFormat(u"application/pdf"));
ASSERT_EQ(SaveFormat::Svg, FileFormatUtil::ContentTypeToSaveFormat(u"image/svg+xml"));
ASSERT_EQ(SaveFormat::Epub, FileFormatUtil::ContentTypeToSaveFormat(u"application/epub+zip"));

// For file types that can be saved and loaded, we can match a media type to both a load format and a save format.
ASSERT_EQ(LoadFormat::Doc, FileFormatUtil::ContentTypeToLoadFormat(u"application/msword"));
ASSERT_EQ(SaveFormat::Doc, FileFormatUtil::ContentTypeToSaveFormat(u"application/msword"));

ASSERT_EQ(LoadFormat::Docx, FileFormatUtil::ContentTypeToLoadFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
ASSERT_EQ(SaveFormat::Docx, FileFormatUtil::ContentTypeToSaveFormat(u"application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

ASSERT_EQ(LoadFormat::Text, FileFormatUtil::ContentTypeToLoadFormat(u"text/plain"));
ASSERT_EQ(SaveFormat::Text, FileFormatUtil::ContentTypeToSaveFormat(u"text/plain"));

ASSERT_EQ(LoadFormat::Rtf, FileFormatUtil::ContentTypeToLoadFormat(u"application/rtf"));
ASSERT_EQ(SaveFormat::Rtf, FileFormatUtil::ContentTypeToSaveFormat(u"application/rtf"));

ASSERT_EQ(LoadFormat::Html, FileFormatUtil::ContentTypeToLoadFormat(u"text/html"));
ASSERT_EQ(SaveFormat::Html, FileFormatUtil::ContentTypeToSaveFormat(u"text/html"));

ASSERT_EQ(LoadFormat::Mhtml, FileFormatUtil::ContentTypeToLoadFormat(u"multipart/related"));
ASSERT_EQ(SaveFormat::Mhtml, FileFormatUtil::ContentTypeToSaveFormat(u"multipart/related"));
```

## See Also

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
