---
title: get_Width
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the width of the text column in points.
type: docs
weight: 14
url: /cpp/aspose.words/textcolumn/get_width/
---
## TextColumn.get_Width method


Gets or sets the width of the text column in points.

```cpp
double Aspose::Words::TextColumn::get_Width()
```


## Examples




Shows how to create unevenly spaced columns. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<PageSetup> pageSetup = builder->get_PageSetup();

SharedPtr<TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Determine the amount of room that we have available for arranging columns.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Set the first column to be narrow.
SharedPtr<TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Set the second column to take the rest of the space available within the margins of the page.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(ArtifactsDir + u"PageSetup.CustomColumnWidth.docx");
```

