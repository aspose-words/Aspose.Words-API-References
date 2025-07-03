---
title: Aspose::Words::TextColumn::get_SpaceAfter method
linktitle: get_SpaceAfter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextColumn::get_SpaceAfter method. Gets or sets the space between this column and the next column in points. Not required for the last column in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/textcolumn/get_spaceafter/
---
## TextColumn::get_SpaceAfter method


Gets or sets the space between this column and the next column in points. Not required for the last column.

```cpp
double Aspose::Words::TextColumn::get_SpaceAfter()
```


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

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
