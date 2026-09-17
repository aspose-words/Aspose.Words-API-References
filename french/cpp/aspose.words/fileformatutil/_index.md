---
title: "classe Aspose::Words::FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::FileFormatUtil. Fournit des méthodes utilitaires pour travailler avec les formats de fichiers, comme la détection du format de fichier ou la conversion des extensions de fichiers vers ou depuis les énumérations de formats de fichiers. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Fournit des méthodes utilitaires pour travailler avec les formats de fichiers, comme la détection du format de fichier ou la conversion des extensions de fichiers vers/depuis les énumérations de formats de fichiers. Pour en savoir plus, consultez l'article de documentation [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatUtil
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Convertit le type de contenu IANA en une valeur d’énumération de format de chargement. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Convertit le type de contenu IANA en une valeur d’énumération de format d’enregistrement. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Détecte et renvoie les informations sur le format d’un document stocké dans un fichier disque. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Détecte et renvoie les informations sur le format d’un document stocké dans un flux. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Convertit une extension de nom de fichier en une valeur [SaveFormat](../saveformat/). |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Convertit une valeur d’énumération de type d’image Aspose.Words en une extension de fichier. L’extension renvoyée est une chaîne en minuscules précédée d’un point. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Convertit une valeur d’énumération de format de chargement en une extension de fichier. L’extension renvoyée est une chaîne en minuscules précédée d’un point. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Convertit une valeur [LoadFormat](../loadformat/) en une valeur [SaveFormat](../saveformat/) si possible. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Convertit une valeur d’énumération de format d’enregistrement en une extension de fichier. L’extension renvoyée est une chaîne en minuscules précédée d’un point. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Convertit une valeur [SaveFormat](../saveformat/) en une valeur [LoadFormat](../loadformat/) si possible. |

## Exemples



Montre comment détecter l’encodage dans un fichier HTML.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// La propriété Encoding n'est utilisée que lorsque nous créons un objet FileFormatInfo pour un document html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
