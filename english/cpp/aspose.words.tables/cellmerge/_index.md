---
title: Aspose::Words::Tables::CellMerge enum
linktitle: CellMerge
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellMerge enum. Specifies how a cell in a table is merged with other cells in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Specifies how a cell in a table is merged with other cells.

```cpp
enum class CellMerge
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | The cell is not merged. |
| First | 1 | The cell is the first cell in a range of merged cells. |
| Previous | 2 | The cell is merged to the previous cell horizontally or vertically. |


## Examples



Shows how to merge table cells vertically. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of vertically merged cells.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insert a cell into the second column of the first row, then end the row.
// Also, configure the builder to disable vertical merging in created cells.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Insert a cell into the first column of the second row.
// Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Insert another independent cell in the second column of the second row.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


Shows how to merge table cells horizontally. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of horizontally merged cells.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insert a cell into the second column of the first row. Instead of adding text contents,
// we will merge this cell with the first cell that we added directly to the left.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Insert two more unmerged cells to the second row.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
