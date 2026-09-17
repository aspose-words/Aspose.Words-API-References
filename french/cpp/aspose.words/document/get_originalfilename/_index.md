---
title: "Aspose::Words::Document::get_OriginalFileName method"
linktitle: "get_OriginalFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_OriginalFileName méthode. Obtient le nom de fichier original du document en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Obtient le nom de fichier original du document.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Remarques


Renvoie **null** si le document a été chargé depuis un flux ou créé vide.

## Exemples



Montre comment récupérer les détails de l'opération de chargement d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Montre comment utiliser les méthodes de [FileFormatUtil](../../fileformatutil/) pour détecter le format d'un document.
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
