---
title: "Aspose::Words::TextColumnCollection::get_Spacing méthode"
linktitle: "get_Spacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextColumnCollection::get_Spacing méthode. Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d’espace entre chaque colonne en points en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d’espace entre chaque colonne en points.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
```


## Exemples



Montre comment créer plusieurs colonnes espacées uniformément dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Voir aussi

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
