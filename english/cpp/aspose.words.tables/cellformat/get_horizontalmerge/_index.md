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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of horizontally merged cells.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insert a cell into the second column of the first row. Instead of adding text contents,
// we will merge this cell with the first cell that we added directly to the left.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(CellMerge::Previous);
builder->EndRow();

// Insert two more unmerged cells to the second row.
builder->get_CellFormat()->set_HorizontalMerge(CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(ArtifactsDir + u"CellFormat.HorizontalMerge.docx");
```


Prints the horizontal and vertical merge type of a cell. 
```cpp
void CheckCellsMerged()
{
    auto doc = MakeObject<Document>(MyDir + u"Table with merged cells.docx");
    SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

    for (const auto& row : System::IterateOver(table->get_Rows()->LINQ_OfType<SharedPtr<Row>>()))
    {
        for (const auto& cell : System::IterateOver(row->get_Cells()->LINQ_OfType<SharedPtr<Cell>>()))
        {
            std::cout << PrintCellMergeType(cell) << std::endl;
        }
    }
}

String PrintCellMergeType(SharedPtr<Cell> cell)
{
    bool isHorizontallyMerged = cell->get_CellFormat()->get_HorizontalMerge() != CellMerge::None;
    bool isVerticallyMerged = cell->get_CellFormat()->get_VerticalMerge() != CellMerge::None;
    String cellLocation = String::Format(u"R{0}, C{1}", cell->get_ParentRow()->get_ParentTable()->IndexOf(cell->get_ParentRow()) + 1,
                                         cell->get_ParentRow()->IndexOf(cell) + 1);

    if (isHorizontallyMerged && isVerticallyMerged)
    {
        return String::Format(u"The cell at {0} is both horizontally and vertically merged", cellLocation);
    }
    if (isHorizontallyMerged)
    {
        return String::Format(u"The cell at {0} is horizontally merged.", cellLocation);
    }

    return isVerticallyMerged ? String::Format(u"The cell at {0} is vertically merged", cellLocation)
                              : String::Format(u"The cell at {0} is not merged", cellLocation);
}
```

## See Also

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
