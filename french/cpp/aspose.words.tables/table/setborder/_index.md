---
title: "Méthode SetBorder de Aspose::Words::Tables::Table"
linktitle: "SetBorder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode SetBorder de Aspose::Words::Tables::Table. Définit la bordure de tableau spécifiée avec le style de ligne, la largeur et la couleur spécifiés en C++."
type: docs
weight: 68000
url: /fr/cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


Définit la bordure de tableau spécifiée avec le style de ligne, la largeur et la couleur spécifiés.

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | La bordure du tableau à modifier. |
| lineStyle | Aspose::Words::LineStyle | Le style de ligne à appliquer. |
| lineWidth | double | La largeur de ligne à définir (en points). |
| color | System::Drawing::Color | La couleur à utiliser pour la bordure. |
| isOverrideCellBorders | bool | Lorsque **true**, supprime toutes les bordures de cellules explicites existantes. |

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

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
