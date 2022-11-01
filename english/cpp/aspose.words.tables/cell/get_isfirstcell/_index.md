---
title: get_IsFirstCell
second_title: Aspose.Words for C++ API Reference
description: True if this is the first cell inside a row; false otherwise.
type: docs
weight: 66
url: /cpp/aspose.words.tables/cell/get_isfirstcell/
---
## Cell.get_IsFirstCell method


True if this is the first cell inside a row; false otherwise.

```cpp
bool Aspose::Words::Tables::Cell::get_IsFirstCell()
```


## Examples




Shows how to print the node structure of every table in a document. 
```cpp
void TableToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::TableStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class TableStructurePrinter : public DocumentVisitor
{
public:
    TableStructurePrinter() : mVisitorIsInsideTable(false), mDocTraversalDepth(0)
    {
        mVisitedTables = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideTable = false;
    }

    String GetText()
    {
        return mVisitedTables->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideTable)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitTableStart(SharedPtr<Table> table) override
    {
        int rows = 0;
        int columns = 0;

        if (table->get_Rows()->get_Count() > 0)
        {
            rows = table->get_Rows()->get_Count();
            columns = table->get_FirstRow()->get_Count();
        }

        IndentAndAppendLine(String(u"[Table start] Size: ") + rows + u"x" + columns);
        mDocTraversalDepth++;
        mVisitorIsInsideTable = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitTableEnd(SharedPtr<Table> table) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Table end]");
        mVisitorIsInsideTable = false;

        return VisitorAction::Continue;
    }

    VisitorAction VisitRowStart(SharedPtr<Row> row) override
    {
        String rowContents = row->GetText().TrimEnd(MakeArray<char16_t>({u'\x0007', u' '})).Replace(u"\u0007", u", ");
        int rowWidth = row->IndexOf(row->get_LastCell()) + 1;
        int rowIndex = row->get_ParentTable()->IndexOf(row);
        String rowStatusInTable = row->get_IsFirstRow() && row->get_IsLastRow() ? u"only"
                                  : row->get_IsFirstRow()                       ? u"first"
                                  : row->get_IsLastRow()                        ? String(u"last")
                                                                                : String(u"");
        if (rowStatusInTable != u"")
        {
            rowStatusInTable = String::Format(u", the {0} row in this table,", rowStatusInTable);
        }

        IndentAndAppendLine(String::Format(u"[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitRowEnd(SharedPtr<Row> row) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Row end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitCellStart(SharedPtr<Cell> cell) override
    {
        SharedPtr<Row> row = cell->get_ParentRow();
        SharedPtr<Table> table = row->get_ParentTable();
        String cellStatusInRow = cell->get_IsFirstCell() && cell->get_IsLastCell() ? u"only"
                                 : cell->get_IsFirstCell()                         ? u"first"
                                 : cell->get_IsLastCell()                          ? String(u"last")
                                                                                   : String(u"");
        if (cellStatusInRow != u"")
        {
            cellStatusInRow = String::Format(u", the {0} cell in this row", cellStatusInRow);
        }

        IndentAndAppendLine(String::Format(u"[Cell start] Row {0}, Col {1}{2}", table->IndexOf(row) + 1, row->IndexOf(cell) + 1, cellStatusInRow));
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitCellEnd(SharedPtr<Cell> cell) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Cell end]");
        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideTable;
    int mDocTraversalDepth;
    SharedPtr<System::Text::StringBuilder> mVisitedTables;

    void IndentAndAppendLine(String text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mVisitedTables->Append(u"|  ");
        }

        mVisitedTables->AppendLine(text);
    }
};
```

