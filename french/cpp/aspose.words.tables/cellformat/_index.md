---
title: "Aspose::Words::Tables::CellFormat classe"
linktitle: "CellFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::CellFormat classe. Représente toute la mise en forme d'une cellule de tableau. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Représente toute la mise en forme d’une cellule de tableau. Pour en savoir plus, consultez l’article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Réinitialise la mise en forme par défaut de la cellule. Ne modifie pas la largeur de la cellule. |
| [get_Borders](./get_borders/)() | Obtient la collection des bordures de la cellule. |
| [get_BottomPadding](./get_bottompadding/)() | Renvoie ou définit la quantité d'espace (en points) à ajouter sous le contenu de la cellule. |
| [get_FitText](./get_fittext/)() | Si **true**, ajuste le texte dans la cellule, en compressant chaque paragraphe à la largeur de la cellule. |
| [get_HideMark](./get_hidemark/)() | Renvoie la visibilité du marqueur de cellule. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Spécifie comment la cellule est fusionnée horizontalement avec d'autres cellules de la ligne. |
| [get_LeftPadding](./get_leftpadding/)() | Renvoie ou définit la quantité d'espace (en points) à ajouter à gauche du contenu de la cellule. |
| [get_Orientation](./get_orientation/)() | Renvoie ou définit l'orientation du texte dans une cellule de tableau. |
| [get_PreferredWidth](./get_preferredwidth/)() | Renvoie ou définit la largeur préférée de la cellule. |
| [get_RightPadding](./get_rightpadding/)() | Renvoie ou définit la quantité d'espace (en points) à ajouter à droite du contenu de la cellule. |
| [get_Shading](./get_shading/)() | Renvoie un objet [Shading](../../aspose.words/shading/) qui fait référence à la mise en forme d'ombrage de la cellule. |
| [get_TopPadding](./get_toppadding/)() | Renvoie ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu de la cellule. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Renvoie ou définit l'alignement vertical du texte dans la cellule. |
| [get_VerticalMerge](./get_verticalmerge/)() | Spécifie comment la cellule est fusionnée avec d'autres cellules verticalement. |
| [get_Width](./get_width/)() | Obtient la largeur de la cellule en points. |
| [get_WrapText](./get_wraptext/)() | Si **true**, enveloppe le texte de la cellule. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Définit la visibilité du marqueur de cellule. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Définisseur pour [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Définit la quantité d'espace (en points) à ajouter à gauche/haut/droite/bas du contenu de la cellule. |
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


Montre comment modifier le formatage d'une cellule de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Utilisez la propriété "CellFormat" d'une cellule pour définir le formatage qui modifie l'apparence de cette cellule.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
