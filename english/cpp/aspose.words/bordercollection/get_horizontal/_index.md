---
title: get_Horizontal
second_title: Aspose.Words for C++ API Reference
description: Gets the horizontal border that is used between cells or conforming paragraphs.
type: docs
weight: 79
url: /cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection.get_Horizontal method


Gets the horizontal border that is used between cells or conforming paragraphs.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## Examples




Shows how to apply settings to horizontal borders to a paragraph's format. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a red horizontal border for the paragraph. Any paragraphs created afterwards will inherit these border settings.
SharedPtr<BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// Write text to the document without creating a new paragraph afterward.
// Since there is no paragraph underneath, the horizontal border will not be visible.
builder->Write(u"Paragraph above horizontal border.");

// Once we add a second paragraph, the border of the first paragraph will become visible.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(ArtifactsDir + u"Border.HorizontalBorders.docx");
```


Shows how to apply settings to vertical borders to a table row's format. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a table with red and blue inner borders.
SharedPtr<Table> table = builder->StartTable();

for (int i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(String::Format(u"Row {0}, Column 2", i + 1));

    SharedPtr<Row> row = builder->EndRow();
    SharedPtr<BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Adjust the appearance of borders that will appear between rows.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Adjust the appearance of borders that will appear between cells.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// A row format, and a cell's inner paragraph use different border settings.
SharedPtr<Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(LineStyle::None, border->get_LineStyle());

doc->Save(ArtifactsDir + u"Border.VerticalBorders.docx");
```

