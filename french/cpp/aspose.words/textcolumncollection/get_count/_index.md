---
title: "Méthode Aspose::Words::TextColumnCollection::get_Count"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::TextColumnCollection::get_Count. Obtient le nombre de colonnes dans la section d'un document en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Obtient le nombre de colonnes dans la section d’un document.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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
