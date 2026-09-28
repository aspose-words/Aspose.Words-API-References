---
title: "Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat метод"
linktitle: "ContentTypeToLoadFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat метод. Преобразует тип содержимого IANA в перечисленное значение формата загрузки в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil::ContentTypeToLoadFormat method


Преобразует тип содержимого IANA в перечисляемое значение формата загрузки.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(const System::String &contentType)
```


## Примеры



Показывает, как найти соответствующий **Aspose** формат загрузки/сохранения для каждой строки типа медиа.
```cpp
// Методы ContentTypeToSaveFormat/ContentTypeToLoadFormat принимают только официальные названия медиа‑типов IANA, также известные как MIME‑типы.
// Все действительные медиа‑типы перечислены здесь: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Попытка связать SaveFormat с частичной строкой типа медиа не будет работать.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
})(), System::ArgumentException);

// Если у Aspose.Words нет соответствующего формата сохранения/загрузки для типа содержимого, также будет выброшено исключение.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
})(), System::ArgumentException);

// Файлы перечисленных ниже типов можно сохранять, но нельзя загружать с помощью Aspose.Words.
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

// Для типов файлов, которые можно сохранять и загружать, мы можем сопоставить тип медиа как формату загрузки, так и формату сохранения.
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

## См. также

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
