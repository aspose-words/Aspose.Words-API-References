---
title: "Méthode Aspose::Words::Tables::Table::SetShading"
linktitle: "SetShading"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::SetShading. Définit l’ombrage aux valeurs spécifiées sur l’ensemble du tableau en C++."
type: docs
weight: 70000
url: /fr/cpp/aspose.words.tables/table/setshading/
---
## Table::SetShading method


Applique l’ombrage aux valeurs spécifiées sur l’ensemble du tableau.

```cpp
void Aspose::Words::Tables::Table::SetShading(Aspose::Words::TextureIndex texture, System::Drawing::Color foregroundColor, System::Drawing::Color backgroundColor)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| texture | Aspose::Words::TextureIndex | La texture à appliquer. |
| foregroundColor | System::Drawing::Color | La couleur de la texture. |
| backgroundColor | System::Drawing::Color | La couleur du remplissage d'arrière-plan. |

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

* Enum [TextureIndex](../../../aspose.words/textureindex/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
