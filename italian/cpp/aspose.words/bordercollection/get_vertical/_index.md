---
title: "Metodo Aspose::Words::BorderCollection::get_Vertical"
linktitle: "get_Vertical"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BorderCollection::get_Vertical. Ottiene il bordo verticale utilizzato tra le celle in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words/bordercollection/get_vertical/
---
## BorderCollection::get_Vertical method


Ottiene il bordo verticale utilizzato tra le celle.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Vertical()
```


## Esempi



Mostra come applicare le impostazioni ai bordi verticali al formato di una riga di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea una tabella con bordi interni rossi e blu.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Regola l'aspetto dei bordi che appariranno tra le righe.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Regola l'aspetto dei bordi che appariranno tra le celle.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// Un formato di riga e il paragrafo interno di una cella usano impostazioni di bordo diverse.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## Vedi anche

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
