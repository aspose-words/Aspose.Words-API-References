---
title: "Méthode Aspose::Words::Drawing::OlePackage::get_FileName"
linktitle: "get_FileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::OlePackage::get_FileName. Obtient ou définit le nom de fichier du paquet OLE en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


Obtient ou définit le nom de fichier du package OLE.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
```


## Exemples



Montre comment insérer un objet OLE dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les objets OLE nous permettent d'ouvrir d'autres fichiers du système de fichiers local en utilisant une autre application installée
// dans notre système d'exploitation en double-cliquant sur la forme qui contient l'objet OLE dans le corps du document.
// Dans ce cas, notre fichier externe sera une archive ZIP.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## Voir aussi

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
