---
title: "Aspose::Words::BorderCollection::get_Horizontal méthode"
linktitle: "get_Horizontal"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_Horizontal méthode. Obtient la bordure horizontale utilisée entre les cellules ou les paragraphes correspondants en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


Obtient la bordure horizontale utilisée entre les cellules ou les paragraphes correspondants.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## Exemples



Montre comment appliquer les paramètres aux bordures horizontales du format d'un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez une bordure horizontale rouge pour le paragraphe. Tous les paragraphes créés ensuite hériteront de ces paramètres de bordure.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// Écrivez du texte dans le document sans créer un nouveau paragraphe par la suite.
// Puisqu'il n'y a pas de paragraphe en dessous, la bordure horizontale ne sera pas visible.
builder->Write(u"Paragraph above horizontal border.");

// Une fois que nous ajoutons un deuxième paragraphe, la bordure du premier paragraphe deviendra visible.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


Montre comment appliquer les paramètres aux bordures verticales du format d'une ligne de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un tableau avec des bordures intérieures rouges et bleues.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Ajustez l'apparence des bordures qui apparaîtront entre les lignes.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Ajustez l'apparence des bordures qui apparaîtront entre les cellules.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// Un format de ligne et le paragraphe interne d'une cellule utilisent des paramètres de bordure différents.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## Voir aussi

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
