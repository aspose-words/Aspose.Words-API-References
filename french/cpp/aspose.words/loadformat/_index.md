---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LoadFormat enum. Indique le format du document qui doit être chargé en C++."
type: docs
weight: 97000
url: /fr/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Indique le format du document qui doit être chargé.

```cpp
enum class LoadFormat
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Auto | 0 | Indique à Aspose.Words de reconnaître le format automatiquement. |
| MsWorks | 8 | Microsoft Works 8 [Document](../document/). |
| Doc | 10 | Microsoft Word 95 ou Word 97 - 2003 [Document](../document/). |
| Dot | 11 | Microsoft Word 95 ou Word 97 - 2003 Modèle. |
| DocPreWord60 | 12 | Le document est au format pré-Word 95. Aspose.Words ne prend actuellement pas en charge le chargement de tels documents. |
| Docx | 20 | Office Open XML WordprocessingML [Document](../document/) (sans macro). |
| Docm | 21 | Office Open XML WordprocessingML avec macro [Document](../document/). |
| Dotx | 22 | Office Open XML WordprocessingML Modèle (sans macro). |
| Dotm | 23 | Office Open XML WordprocessingML Modèle avec macro. |
| FlatOpc | 24 | Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML avec macro [Document](../document/) stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| FlatOpcTemplate | 26 | Office Open XML WordprocessingML Modèle (sans macro) stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | Office Open XML WordprocessingML Modèle avec macro stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| Rtf | 30 | Format RTF. |
| WordML | 31 | format WordprocessingML de Microsoft Word 2003. |
| Html | 50 | Format HTML. |
| Mhtml | 51 | Format MHTML (archive Web). |
| Mobi | 52 | Format MOBI. Utilisé par le lecteur MobiPocket et les lecteurs Amazon Kindle. |
| Chm | 53 | Format CHM (Aide HTML compilée). |
| Azw3 | 54 | Format AZW3. Utilisé par les lecteurs Amazon Kindle. |
| Epub | 55 | Format EPUB. |
| Odt | 60 | Texte ODF [Document](../document/). |
| Ott | 61 | Modèle de [Document](../document/) texte ODF. |
| Texte | 62 | Texte brut. |
| Markdown | 63 | Document texte Markdown. |
| Xml | 65 | Document XML. |
| Unknown | 255 | Format non reconnu, impossible de le charger avec [Aspose.Words](../). |


## Exemples



Montre comment utiliser les méthodes de [FileFormatUtil](../fileformatutil/) pour détecter le format d'un document.
```cpp
// Chargez un document à partir d'un fichier sans extension, puis détectez son format de fichier.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Voici deux méthodes pour convertir un LoadFormat en son SaveFormat correspondant.
    // 1 -  Obtenez la chaîne d'extension de fichier pour le LoadFormat, puis obtenez le SaveFormat correspondant à partir de cette chaîne :
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Convertissez directement le LoadFormat en son SaveFormat :
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Chargez un document depuis le flux, puis enregistrez-le avec l'extension détectée automatiquement.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


Montre comment spécifier une URI de base lors de l'ouverture d'un document html.
```cpp
// Supposons que nous voulions charger un document .html contenant une image liée par une URI relative
// alors que l'image se trouve à un autre emplacement. Dans ce cas, nous devrons résoudre l'URI relative en une URI absolue.
// Nous pouvons fournir une URI de base en utilisant un objet HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Bien que l'image était cassée dans le .html d'entrée, notre URI de base personnalisée nous a aidés à réparer le lien.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Ce document de sortie affichera l'image qui manquait.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
