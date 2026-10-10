---
title: "Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat metodu"
linktitle: "ContentTypeToLoadFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat metodu. C++'ta IANA içerik tipini bir yükleme formatı sayısal değerine dönüştürür."
type: docs
weight: 1000
url: /tr/cpp/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil::ContentTypeToLoadFormat method


IANA içerik tipini bir yükleme formatı enum değerine dönüştürür.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(const System::String &contentType)
```


## Örnekler



Her medya türü dizesinden karşılık gelen **Aspose** yükleme/kaydetme formatını nasıl bulacağınızı gösterir.
```cpp
// ContentTypeToSaveFormat/ContentTypeToLoadFormat metodları yalnızca resmi IANA medya türü adlarını, yani MIME tiplerini kabul eder.
// Tüm geçerli medya türleri burada listelenmiştir: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Bir SaveFormat'ı kısmi bir medya türü dizesiyle ilişkilendirmeye çalışmak işe yaramaz.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
})(), System::ArgumentException);

// Aspose.Words bir içerik türü için karşılık gelen kaydet/yük formatına sahip değilse, bir istisna da fırlatılacaktır.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
})(), System::ArgumentException);

// Aşağıda listelenen türdeki dosyalar kaydedilebilir, ancak Aspose.Words kullanılarak yüklenemez.
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

// Kaydedilebilen ve yüklenebilen dosya türleri için, bir medya türünü hem yük formatına hem de kaydet formatına eşleştirebiliriz.
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

## Ayrıca Bakınız

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
