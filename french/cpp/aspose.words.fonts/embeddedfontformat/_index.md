---
title: "Aspose::Words::Fonts::EmbeddedFontFormat enum"
linktitle: "EmbeddedFontFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. Spécifie le format d’une police incorporée particulière à l’intérieur de l’objet FontInfo. Lors de l’enregistrement d’un document dans un fichier, seules les polices incorporées du format correspondant sont écrites en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Spécifie le format d’une police incorporée particulière à l’intérieur de l’objet [FontInfo](../fontinfo/). Lors de l’enregistrement d’un document dans un fichier, seules les polices incorporées du format correspondant sont écrites.

```cpp
enum class EmbeddedFontFormat
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Spécifie le format de fichier Embedded OpenType (EOT). Ce format de polices incorporées est utilisé dans les fichiers DOC. |
| OpenType | 1 | Spécifie la police, incorporée comme copie brute du fichier de police OpenType (TrueType). Ce format de polices incorporées est utilisé dans le format Open Office XML, y compris les fichiers DOCX. |


## Exemples



Montre comment extraire une police intégrée d'un document et l'enregistrer sur le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Les formats de police intégrée peuvent différer dans d'autres formats tels que .doc.
// Nous devons connaître le format correct avant de pouvoir extraire la police.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// De plus, nous pouvons convertir le format OpenType intégré, provenant de documents .doc, en OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
