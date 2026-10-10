---
title: "Aspose::Words::Drawing::OlePackage class"
linktitle: "OlePackage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OlePackage class. Permet d'accéder aux propriétés du package OLE. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Permet d'accéder aux propriétés du package OLE. Pour en savoir plus, consultez l'article de documentation [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) .

```cpp
class OlePackage : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Obtient ou définit le nom d'affichage du package OLE. |
| [get_FileName](./get_filename/)() const | Obtient ou définit le nom de fichier du package OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Définisseur pour [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Définisseur pour [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
