---
title: "Aspose::Words::BorderCollection::get_Vertical méthode"
linktitle: "get_Vertical"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_Vertical méthode. Obtient la bordure verticale utilisée entre les cellules en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words/bordercollection/get_vertical/
---
## BorderCollection::get_Vertical method


Obtient la bordure verticale utilisée entre les cellules.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Vertical()
```


## Exemples



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
