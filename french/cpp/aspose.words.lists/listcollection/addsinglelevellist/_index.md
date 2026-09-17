---
title: "Méthode Aspose::Words::Lists::ListCollection::AddSingleLevelList"
linktitle: "AddSingleLevelList"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Lists::ListCollection::AddSingleLevelList. Crée une nouvelle liste à un seul niveau basée sur le modèle prédéfini et l’ajoute à la collection de listes du document en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Crée une nouvelle liste à un seul niveau basée sur le modèle prédéfini et l'ajoute à la collection de listes du document.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Exemples



Montre comment créer une nouvelle liste à un seul niveau basée sur le modèle prédéfini.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Crée la liste à puces à partir du modèle BulletCircle.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Écrit la liste à puces dans le document résultant.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Crée la liste numérotée à partir du modèle NumberUppercaseLetterDot.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Écrit la liste numérotée dans le document résultant.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## Voir aussi

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
