---
title: Aspose::Words::TextColumn class
linktitle: TextColumn
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextColumn class. Represents a single text column. TextColumn is a member of the TextColumnCollection collection. The TextColumn collection includes all the columns in a section of a document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 70000
url: /cpp/aspose.words/textcolumn/
---
## TextColumn class


Represents a single text column. [TextColumn](./) is a member of the [TextColumnCollection](../textcolumncollection/) collection. The [TextColumn](./) collection includes all the columns in a section of a document. To learn more, visit the [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) documentation article.

```cpp
class TextColumn : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Gets or sets the space between this column and the next column in points. Not required for the last column. |
| [get_Width](./get_width/)() | Gets or sets the width of the text column in points. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Setter for [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Setter for [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Remarks


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

When a new [TextColumn](./) is created it has its width and spacing set to zero.

## Examples



Shows how to create unevenly spaced columns. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Determine the amount of room that we have available for arranging columns.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Set the first column to be narrow.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Set the second column to take the rest of the space available within the margins of the page.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
