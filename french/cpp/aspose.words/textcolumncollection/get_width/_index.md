---
title: "Méthode Aspose::Words::TextColumnCollection::get_Width"
linktitle: "get_Width"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::TextColumnCollection::get_Width. Lorsque les colonnes sont espacées uniformément, obtient la largeur des colonnes en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/textcolumncollection/get_width/
---
## TextColumnCollection::get_Width method


Lorsque les colonnes sont espacées uniformément, obtient la largeur des colonnes.

```cpp
double Aspose::Words::TextColumnCollection::get_Width()
```

## Remarques


N’a d’effet que lorsque [EvenlySpaced](../get_evenlyspaced/) est défini sur **true**.

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
