---
title: "Metodo Aspose::Words::BorderCollection::get_Horizontal"
linktitle: "get_Horizontal"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BorderCollection::get_Horizontal. Ottiene il bordo orizzontale utilizzato tra le celle o i paragrafi corrispondenti in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


Ottiene il bordo orizzontale utilizzato tra le celle o i paragrafi corrispondenti.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## Esempi



Mostra come applicare le impostazioni ai bordi orizzontali al formato di un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un bordo orizzontale rosso per il paragrafo. Qualsiasi paragrafo creato successivamente erediterà queste impostazioni del bordo.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// Scrivi del testo nel documento senza creare un nuovo paragrafo successivamente.
// Poiché non c'è alcun paragrafo sottostante, il bordo orizzontale non sarà visibile.
builder->Write(u"Paragraph above horizontal border.");

// Una volta aggiunto un secondo paragrafo, il bordo del primo paragrafo diventerà visibile.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


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
