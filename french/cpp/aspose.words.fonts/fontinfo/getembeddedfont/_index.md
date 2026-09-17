---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont méthode"
linktitle: "GetEmbeddedFont"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont méthode. Obtient un fichier de police intégré spécifique en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo::GetEmbeddedFont method


Obtient un fichier de police incorporé spécifique.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat format, Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| format | Aspose::Words::Fonts::EmbeddedFontFormat | Spécifie le format de police à récupérer. |
| style | Aspose::Words::Fonts::EmbeddedFontStyle | Spécifie le style de police à récupérer. |

### ReturnValue

Renvoie **null** si la police spécifiée n'est pas intégrée.

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

* Enum [EmbeddedFontFormat](../../embeddedfontformat/)
* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
