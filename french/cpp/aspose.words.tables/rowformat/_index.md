---
title: "Classe Aspose::Words::Tables::RowFormat"
linktitle: "RowFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Tables::RowFormat. Représente toute la mise en forme d'une ligne de table. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


Représente toute la mise en forme d’une ligne de tableau. Pour en savoir plus, consultez l’article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Réinitialise la mise en forme de ligne par défaut. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Vrai si le texte d'une ligne de table est autorisé à se diviser à travers un saut de page. |
| [get_Borders](./get_borders/)() | Obtient la collection des bordures de cellule par défaut pour la ligne. |
| [get_HeadingFormat](./get_headingformat/)() | Vrai si la ligne est répétée comme en-tête de table sur chaque page lorsque la table s'étend sur plusieurs pages. |
| [get_Height](./get_height/)() | Obtient ou définit la hauteur de la ligne de table en points. |
| [get_HeightRule](./get_heightrule/)() | Obtient ou définit la règle de détermination de la hauteur de la ligne de table. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Définisseur pour [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | Définisseur pour [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | Définisseur pour [Aspose::Words::Tables::RowFormat::get_Height](./get_height/). |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | Définisseur pour [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment construire un tableau avec des bordures personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Définition des options de formatage de tableau pour un DocumentBuilder
// les appliquera à chaque ligne et cellule que nous ajoutons avec celui‑ci.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Modifier le formatage l'appliquera à la cellule actuelle,
// et à toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Augmentez la hauteur de la ligne pour adapter le texte vertical.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Montre comment modifier le format des lignes et des cellules d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Utilisez la propriété "RowFormat" de la première ligne pour modifier le formatage
// du contenu de toutes les cellules de cette ligne.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Utilisez la propriété "CellFormat" de la première cellule de la dernière ligne pour modifier le formatage du contenu de cette cellule.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Montre comment modifier le formatage d'une ligne de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Utilisez la propriété "RowFormat" de la première ligne pour définir un formatage qui modifie l'apparence de toute la ligne.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
