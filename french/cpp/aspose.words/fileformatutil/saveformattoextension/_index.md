---
title: "Aspose::Words::FileFormatUtil::SaveFormatToExtension méthode"
linktitle: "SaveFormatToExtension"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileFormatUtil::SaveFormatToExtension méthode. Convertit une valeur d'énumération de format d'enregistrement en une extension de fichier. L'extension retournée est une chaîne en minuscules avec un point initial en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil::SaveFormatToExtension method


Convertit une valeur d’énumération de format d’enregistrement en une extension de fichier. L’extension renvoyée est une chaîne en minuscules précédée d’un point.

```cpp
static System::String Aspose::Words::FileFormatUtil::SaveFormatToExtension(Aspose::Words::SaveFormat saveFormat)
```

## Remarques


La valeur [WordML](../../saveformat/) est convertie en ".wml".

La valeur [FlatOpc](../../saveformat/) est convertie en ".fopc".

## Exemples



Montre comment utiliser les méthodes [FileFormatUtil](../) pour détecter le format d'un document.
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

## Voir aussi

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
