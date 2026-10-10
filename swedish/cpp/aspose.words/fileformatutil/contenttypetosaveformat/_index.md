---
title: "Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat metod"
linktitle: "ContentTypeToSaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat metod. Konverterar IANA‑innehållstyp till ett spara‑format‑enumerationsvärde i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil::ContentTypeToSaveFormat method


Konverterar IANA‑innehållstyp till ett sparformat‑enumerationsvärde.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(const System::String &contentType)
```


## Exempel



Visar hur man hittar motsvarande **Aspose** läs-/sparaformat från varje mediatypsträng.
```cpp
// Metoderna ContentTypeToSaveFormat/ContentTypeToLoadFormat accepterar endast officiella IANA-medietypnamn, även kända som MIME-typer.
// Alla giltiga mediatyper listas här: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Att försöka associera ett SaveFormat med en partiell mediatypsträng kommer inte att fungera.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
})(), System::ArgumentException);

// Om Aspose.Words inte har ett motsvarande spara/läsformat för en innehållstyp, kommer ett undantag också att kastas.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
})(), System::ArgumentException);

// Filer av typerna som listas nedan kan sparas, men inte läsas med Aspose.Words.
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

// För filtyper som kan sparas och läsas kan vi matcha en mediatyp till både ett läsformat och ett sparaformat.
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

## Se även

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
