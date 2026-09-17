---
title: "Aspose::Words::TextureIndex enum"
linktitle: "TextureIndex"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextureIndex enum. Spécifie la texture d'ombrage en C++."
type: docs
weight: 125000
url: /fr/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Spécifie la texture d'ombrage.

```cpp
enum class TextureIndex
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Texture22Pt5Percent | 40 |  |
| Texture25Percent | 5 |  |
| Texture27Pt5Percent | 41 |  |
| Texture2Pt5Percent | 35 |  |
| Texture30Percent | 6 |  |
| Texture32Pt5Percent | 42 |  |
| Texture35Percent | 43 |  |
| Texture37Pt5Pourcent | 44 |  |
| Texture40Pourcent | 7 |  |
| Texture42Pt5Pourcent | 45 |  |
| Texture45Pourcent | 46 |  |
| Texture47Pt5Pourcent | 47 |  |
| Texture50Pourcent | 8 |  |
| Texture52Pt5Pourcent | 48 |  |
| Texture55Pourcent | 49 |  |
| Texture57Pt5Pourcent | 50 |  |
| Texture5Pourcent | 2 |  |
| Texture60Pourcent | 9 |  |
| Texture62Pt5Pourcent | 51 |  |
| Texture65Pourcent | 52 |  |
| Texture67Pt5Pourcent | 53 |  |
| Texture70Pourcent | 10 |  |
| Texture72Pt5Pourcent | 54 |  |
| Texture75Pourcent | 11 |  |
| Texture77Pt5Pourcent | 55 |  |
| Texture7Pt5Pourcent | 36 |  |
| Texture80Pourcent | 12 |  |
| Texture82Pt5Pourcent | 56 |  |
| Texture85Pourcent | 57 |  |
| Texture87Pt5Pourcent | 58 |  |
| Texture90Pourcent | 13 |  |
| Texture92Pt5Pourcent | 59 |  |
| Texture95Percent | 60 |  |
| Texture97Pt5Percent | 61 |  |
| TextureCross | 24 |  |
| TextureDarkCross | 18 |  |
| TextureDarkDiagonalCross | 19 |  |
| TextureDarkDiagonalDown | 16 |  |
| TextureDarkDiagonalUp | 17 |  |
| TextureDarkHorizontal | 14 |  |
| TextureDarkVertical | 15 |  |
| TextureDiagonalCross | 25 |  |
| TextureDiagonalDown | 22 |  |
| TextureDiagonalUp | 23 |  |
| TextureHorizontal | 20 |  |
| TextureNone | 0 |  |
| TextureSolid | 1 |  |
| TextureVertical | 21 |  |
| TextureNil | 65535 | Spécifie qu'aucun motif ne doit être utilisé sur la région ombrée actuelle (c.-à-d. le motif doit être un remplissage complet avec la couleur d'arrière-plan). |


## Exemples



Montre comment décorer le texte avec des bordures et de l’ombrage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
