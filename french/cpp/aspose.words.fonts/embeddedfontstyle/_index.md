---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. Spécifie le style d’une police incorporée à l’intérieur d’un objet FontInfo en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Spécifie le style d’une police incorporée à l’intérieur d’un objet [FontInfo](../fontinfo/).

```cpp
enum class EmbeddedFontStyle
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Regular | 0 | Spécifie la police incorporée Regular. |
| Gras | 1 | Spécifie la police intégrée Gras. |
| Italique | 2 | Spécifie la police intégrée Italique. |
| GrasItalique | 3 | Spécifie la police intégrée Gras-Italique. |


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
