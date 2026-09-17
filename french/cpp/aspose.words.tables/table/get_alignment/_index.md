---
title: "Méthode Aspose::Words::Tables::Table::get_Alignment"
linktitle: "get_Alignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::get_Alignment. Spécifie comment un tableau en ligne est aligné dans le document en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.tables/table/get_alignment/
---
## Table::get_Alignment method


Spécifie comment un tableau en ligne est aligné dans le document.

```cpp
Aspose::Words::Tables::TableAlignment Aspose::Words::Tables::Table::get_Alignment()
```

## Remarques


La valeur par défaut est [Left](../../tablealignment/).

## Exemples



Montre comment appliquer une bordure de contour à un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Alignez le tableau au centre de la page.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Effacez toutes les bordures et ombrages existants du tableau.
table->ClearBorders();
table->ClearShading();

// Ajoutez des bordures vertes au contour du tableau.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Remplissez les cellules avec une couleur unie vert clair.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Voir aussi

* Enum [TableAlignment](../../tablealignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
