---
title: Aspose::Words::Tables::CellFormat::get_HorizontalMerge method
linktitle: get_HorizontalMerge
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellFormat::get_HorizontalMerge method. Specifies how the cell is merged horizontally with other cells in the row in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Specifies how the cell is merged horizontally with other cells in the row.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Examples



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

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
