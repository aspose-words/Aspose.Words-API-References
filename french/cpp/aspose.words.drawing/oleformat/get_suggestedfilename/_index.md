---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName méthode"
linktitle: "get_SuggestedFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName méthode. Obtient le nom de fichier suggéré pour l'objet intégré actuel si vous souhaitez l'enregistrer dans un fichier en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Obtient le nom de fichier suggéré pour l'objet incorporé actuel si vous souhaitez l'enregistrer dans un fichier.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Exemples



Montre comment obtenir le nom de fichier suggéré d'un objet OLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// Les objets OLE peuvent fournir un nom de fichier et une extension suggérés,
// que nous pouvons utiliser lors de l'enregistrement du contenu de l'objet dans un fichier du système de fichiers local.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
