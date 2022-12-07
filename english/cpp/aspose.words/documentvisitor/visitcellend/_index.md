---
title: VisitCellEnd
second_title: Aspose.Words for C++ API Reference
description: Called when enumeration of a table cell has ended.
type: docs
weight: 131
url: /cpp/aspose.words/documentvisitor/visitcellend/
---
## DocumentVisitor::VisitCellEnd method


Called when enumeration of a table cell has ended.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitCellEnd(System::SharedPtr<Aspose::Words::Tables::Cell> cell)
```


| Parameter | Type | Description |
| --- | --- | --- |
| cell | System::SharedPtr\<Aspose::Words::Tables::Cell\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

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


Shows how to use a [DocumentVisitor](../) implementation to remove all hidden content from a document. 
```cpp
void RemoveHiddenContentFromDocument()
{
    auto doc = MakeObject<Document>(MyDir + u"Hidden content.docx");

    auto hiddenContentRemover = MakeObject<ExFont::RemoveHiddenContentVisitor>();

    // Below are three types of fields which can accept a document visitor,
    // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
    // 1 -  Paragraph node:
    auto para = System::DynamicCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 4, true));
    para->Accept(hiddenContentRemover);

    // 2 -  Table node:
    SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
    table->Accept(hiddenContentRemover);

    // 3 -  Document node:
    doc->Accept(hiddenContentRemover);

    doc->Save(ArtifactsDir + u"Font.RemoveHiddenContentFromDocument.docx");
}

class RemoveHiddenContentVisitor : public DocumentVisitor
{
public:
    VisitorAction VisitFieldStart(SharedPtr<FieldStart> fieldStart) override
    {
        if (fieldStart->get_Font()->get_Hidden())
        {
            fieldStart->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        if (fieldEnd->get_Font()->get_Hidden())
        {
            fieldEnd->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldSeparator(SharedPtr<FieldSeparator> fieldSeparator) override
    {
        if (fieldSeparator->get_Font()->get_Hidden())
        {
            fieldSeparator->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (run->get_Font()->get_Hidden())
        {
            run->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitParagraphStart(SharedPtr<Paragraph> paragraph) override
    {
        if (paragraph->get_ParagraphBreakFont()->get_Hidden())
        {
            paragraph->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFormField(SharedPtr<FormField> formField) override
    {
        if (formField->get_Font()->get_Hidden())
        {
            formField->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitGroupShapeStart(SharedPtr<GroupShape> groupShape) override
    {
        if (groupShape->get_Font()->get_Hidden())
        {
            groupShape->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeStart(SharedPtr<Shape> shape) override
    {
        if (shape->get_Font()->get_Hidden())
        {
            shape->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitCommentStart(SharedPtr<Comment> comment) override
    {
        if (comment->get_Font()->get_Hidden())
        {
            comment->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFootnoteStart(SharedPtr<Footnote> footnote) override
    {
        if (footnote->get_Font()->get_Hidden())
        {
            footnote->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitSpecialChar(SharedPtr<SpecialChar> specialChar) override
    {
        if (specialChar->get_Font()->get_Hidden())
        {
            specialChar->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitTableEnd(SharedPtr<Table> table) override
    {
        // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
        // If this table had nothing but hidden content, this visitor would have removed all of it,
        // and there would be no child nodes left.
        // Thus, we can also treat the table itself as hidden content and remove it.
        // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
        // which this visitor will not remove.
        if (!table->get_HasChildNodes())
        {
            table->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitCellEnd(SharedPtr<Cell> cell) override
    {
        if (!cell->get_HasChildNodes() && cell->get_ParentNode() != nullptr)
        {
            cell->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitRowEnd(SharedPtr<Row> row) override
    {
        if (!row->get_HasChildNodes() && row->get_ParentNode() != nullptr)
        {
            row->Remove();
        }

        return VisitorAction::Continue;
    }
};
```

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
