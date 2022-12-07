---
title: get_EvenlySpaced
second_title: Aspose.Words for C++ API Reference
description: True if text columns are of equal width and evenly spaced.
type: docs
weight: 27
url: /cpp/aspose.words/textcolumncollection/get_evenlyspaced/
---
## TextColumnCollection::get_EvenlySpaced method


True if text columns are of equal width and evenly spaced.

```cpp
bool Aspose::Words::TextColumnCollection::get_EvenlySpaced()
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

## See Also

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
