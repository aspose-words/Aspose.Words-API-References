---
title: get_VerticalMerge
second_title: Aspose.Words for C++ API Reference
description: Specifies how the cell is merged with other cells vertically.
type: docs
weight: 170
url: /cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Specifies how the cell is merged with other cells vertically.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Remarks


Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated. The consolidated area is used to display the contents of the first vertically merged cell and all other vertically merged cells must be empty.

## Examples



Shows how to merge table cells vertically. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of vertically merged cells.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insert a cell into the second column of the first row, then end the row.
// Also, configure the builder to disable vertical merging in created cells.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Insert a cell into the first column of the second row.
// Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::Previous);

// Insert another independent cell in the second column of the second row.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(ArtifactsDir + u"CellFormat.VerticalMerge.docx");
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
* Library [Aspose.Words](../../../)
