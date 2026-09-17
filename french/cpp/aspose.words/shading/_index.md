---
title: "Classe Aspose::Words::Shading"
linktitle: "Shading"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Shading. Contient les attributs d’ombrage pour un objet. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 60000
url: /fr/cpp/aspose.words/shading/
---
## Shading class


Contient les attributs d'ombrage pour un objet. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Supprime l’ombrage de l’objet. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Détermine si le [Shading](./) spécifié est égal en valeur au [Shading](./) actuel. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Obtient ou définit la couleur appliquée à l’arrière-plan de l’objet [Shading](./). |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Obtient ou définit la couleur du thème du motif d’arrière-plan dans le schéma de couleurs appliqué associé à cet objet [Shading](./). |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur du thème d’arrière-plan. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Obtient ou définit la couleur appliquée au premier plan de l'objet [Shading](./). |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Obtient ou définit la couleur de thème du motif de premier plan dans le schéma de couleurs appliqué associé à cet objet [Shading](./). |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan. |
| [get_Texture](./get_texture/)() | Obtient ou définit la texture de l’ombrage. |
| [GetHashCode](./gethashcode/)() const override | Servit de fonction de hachage pour ce type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Définisseur pour [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | Définisseur pour [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Définisseur pour [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | Définisseur pour [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Définisseur pour [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment appliquer la couleur de bordure et d’ombrage lors de la création d’une table.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Démarrez une table et définissez une couleur/épaisseur par défaut pour ses bordures.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Créez une ligne avec deux cellules ayant des couleurs d’arrière-plan différentes.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Réinitialisez le formatage des cellules pour désactiver les couleurs d’arrière-plan
// définissez une épaisseur de bordure personnalisée pour toutes les nouvelles cellules créées par le constructeur,
// puis construisez une deuxième ligne.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


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

## Voir aussi

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
