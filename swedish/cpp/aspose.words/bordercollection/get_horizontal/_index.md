---
title: "Aspose::Words::BorderCollection::get_Horizontal metod"
linktitle: "get_Horizontal"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection::get_Horizontal metod. Hämtar den horisontella kanten som används mellan celler eller sammanhängande stycken i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


Hämtar den horisontella kanten som används mellan celler eller motsvarande stycken.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## Exempel



Visar hur man tillämpar inställningar på horisontella kanter i ett styckeformat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en röd horisontell kant för stycket. Alla stycken som skapas därefter kommer att ärva dessa kantinställningar.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// Skriv text till dokumentet utan att skapa ett nytt stycke efteråt.
// Eftersom det inte finns något stycke under, kommer den horisontella kanten inte att vara synlig.
builder->Write(u"Paragraph above horizontal border.");

// När vi lägger till ett andra stycke blir kanten på det första stycket synlig.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


Visar hur man tillämpar inställningar på vertikala kanter i ett tabellradsformat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en tabell med röda och blå inre kanter.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Justera utseendet på kanter som kommer att visas mellan rader.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Justera utseendet på kanter som kommer att visas mellan celler.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// Ett radformat och ett cells inre stycke använder olika kantinställningar.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## Se även

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
