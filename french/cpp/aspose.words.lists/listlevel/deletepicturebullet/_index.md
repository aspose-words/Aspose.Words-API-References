---
title: "Méthode Aspose::Words::Lists::ListLevel::DeletePictureBullet"
linktitle: "DeletePictureBullet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Lists::ListLevel::DeletePictureBullet. Supprime le puce image pour le niveau de liste actuel en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel::DeletePictureBullet method


Supprime la puce image du niveau de liste actuel.

```cpp
void Aspose::Words::Lists::ListLevel::DeletePictureBullet()
```


## Exemples



Montre comment définir une icône d'image personnalisée pour les libellés d'éléments de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Créez une puce image pour le niveau de liste actuel, et définissez une image depuis le système de fichiers local
// comme l'icône que les puces de ce niveau de liste afficheront.
list->get_ListLevels()->idx_get(0)->CreatePictureBullet();
list->get_ListLevels()->idx_get(0)->get_ImageData()->SetImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_TRUE(list->get_ListLevels()->idx_get(0)->get_ImageData()->get_HasImage());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

doc->Save(get_ArtifactsDir() + u"Lists.CreatePictureBullet.docx");

list->get_ListLevels()->idx_get(0)->DeletePictureBullet();

ASSERT_TRUE(System::TestTools::IsNull(list->get_ListLevels()->idx_get(0)->get_ImageData()));
```

## Voir aussi

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
