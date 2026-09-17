---
title: "Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat méthode"
linktitle: "LoadFormatToSaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat méthode. Convertit une valeur LoadFormat en une valeur SaveFormat si possible en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil::LoadFormatToSaveFormat method


Convertit une valeur [LoadFormat](../../loadformat/) en une valeur [SaveFormat](../../saveformat/) si possible.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(Aspose::Words::LoadFormat loadFormat)
```


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
* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
