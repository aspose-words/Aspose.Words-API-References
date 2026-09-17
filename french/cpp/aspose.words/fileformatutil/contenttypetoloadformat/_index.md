---
title: "Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat méthode"
linktitle: "ContentTypeToLoadFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat méthode. Convertit le type de contenu IANA en une valeur énumérée de format de chargement en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil::ContentTypeToLoadFormat method


Convertit le type de contenu IANA en une valeur d’énumération de format de chargement.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::ContentTypeToLoadFormat(const System::String &contentType)
```


## Exemples



Montre comment trouver le format de chargement/enregistrement **Aspose** correspondant à chaque chaîne de type média.
```cpp
// Les méthodes ContentTypeToSaveFormat/ContentTypeToLoadFormat n'acceptent que les noms officiels de types média IANA, également appelés types MIME.
// Tous les types média valides sont répertoriés ici : https://www.iana.org/assignments/media-types/media-types.xhtml.

// Essayer d'associer un SaveFormat à une chaîne de type média partielle ne fonctionnera pas.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"jpeg");
})(), System::ArgumentException);

// Si Aspose.Words ne possède pas de format d'enregistrement/chargement correspondant pour un type de contenu, une exception sera également levée.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::ContentTypeToSaveFormat(u"application/zip");
})(), System::ArgumentException);

// Les fichiers des types répertoriés ci-dessous peuvent être enregistrés, mais pas chargés avec Aspose.Words.
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

// Pour les types de fichiers qui peuvent être enregistrés et chargés, nous pouvons associer un type média à la fois à un format de chargement et à un format d'enregistrement.
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

## Voir aussi

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
