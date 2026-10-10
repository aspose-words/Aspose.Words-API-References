---
title: "Aspose::Words::Tables::TableAlignment enum"
linktitle: "TableAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::TableAlignment enum. Spécifie l'alignement d'un tableau en ligne en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


Spécifie l'alignement d'un tableau en ligne.

```cpp
enum class TableAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Gauche | 0 | Le tableau est aligné à gauche. |
| Centre | 1 | Le tableau est centré. |
| Droite | 2 | Le tableau est aligné à droite. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
