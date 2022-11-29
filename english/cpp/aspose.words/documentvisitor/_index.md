---
title: DocumentVisitor
second_title: Aspose.Words for C++ API Reference
description: Base class for custom document visitors.
type: docs
weight: 287
url: /cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Base class for custom document visitors.

```cpp
class DocumentVisitor : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Called when a [AbsolutePositionTab](../absolutepositiontab/) node is encountered in the document. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Called when enumeration of the main text story in a section has ended. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Called when enumeration of the main text story in a section has started. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Called when an end of a bookmark is encountered in the document. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Called when a start of a bookmark is encountered in the document. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Called when enumeration of a building block has ended. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Called when enumeration of a building block has started. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Called when enumeration of a table cell has ended. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Called when enumeration of a table cell has started. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Called when enumeration of a comment text has ended. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Called when the end of a commented range of text is encountered. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Called when the start of a commented range of text is encountered. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Called when enumeration of a comment text has started. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Called when enumeration of the document has finished. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Called when enumeration of the document has started. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Called when an end of an editable range is encountered in the document. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Called when a start of an editable range is encountered in the document. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Called when a field ends in the document. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Called when a field separator is encountered in the document. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Called when a field starts in the document. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Called when enumeration of a footnote or endnote text has ended. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Called when enumeration of a footnote or endnote text has started. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Called when a form field is encountered in the document. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Called when enumeration of a glossary document has ended. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Called when enumeration of a glossary document has started. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Called when enumeration of a group shape has ended. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Called when enumeration of a group shape has started. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Called when enumeration of a header or footer in a section has ended. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Called when enumeration of a header or footer in a section has started. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Called when enumeration of a Office [Math](../../aspose.words.math/) object has ended. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Called when enumeration of a Office [Math](../../aspose.words.math/) object has started. |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Called when enumeration of a paragraph has ended. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Called when enumeration of a paragraph has started. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Called when enumeration of a table row has ended. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Called when enumeration of a table row has started. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Called when a run of text in the is encountered. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Called when enumeration of a section has ended. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Called when enumeration of a section has started. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Called when enumeration of a shape has ended. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Called when enumeration of a shape has started. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Called when enumeration of a smart tag has ended. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Called when enumeration of a smart tag has started. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Called when a [SpecialChar](../specialchar/) node is encountered in the document. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Called when enumeration of a structured document tag has ended. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) |  |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) |  |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Called when enumeration of a structured document tag has started. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Called when a subDocument is encountered. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Called when enumeration of a table has ended. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Called when enumeration of a table has started. |
## Remarks


With **DocumentVisitor** you can define and execute custom operations that require enumeration over the document tree.

For example, Aspose.Words uses **DocumentVisitor** internally for saving **Document** in various formats and for other operations like finding fields or bookmarks over a fragment of a document.

To use **DocumentVisitor**:

1. Create a class derived from **DocumentVisitor**.
1. Override and provide implementations for some or all of the VisitXXX methods to perform some custom operations.
1. Call [Node.Accept](../node/accept/) on the **Node** that you want to start the enumeration from.



**DocumentVisitor** provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

For more information see the Visitor design pattern.

## Examples



Shows how to use a document visitor to print a document's node structure. 
```cpp
void DocStructureToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::DocStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class DocStructurePrinter : public DocumentVisitor
{
public:
    DocStructurePrinter() : mDocTraversalDepth(0)
    {
        mAcceptingNodeChildTree = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mAcceptingNodeChildTree->ToString();
    }

    VisitorAction VisitDocumentStart(SharedPtr<Document> doc) override
    {
        int childNodeCount = doc->GetChildNodes(NodeType::Any, true)->get_Count();

        IndentAndAppendLine(String(u"[Document start] Child nodes: ") + childNodeCount);
        mDocTraversalDepth++;

        // Allow the visitor to continue visiting other nodes.
        return VisitorAction::Continue;
    }

    VisitorAction VisitDocumentEnd(SharedPtr<Document> doc) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Document end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitSectionStart(SharedPtr<Section> section) override
    {
        // Get the index of our section within the document.
        SharedPtr<NodeCollection> docSections = section->get_Document()->GetChildNodes(NodeType::Section, false);
        int sectionIndex = docSections->IndexOf(section);

        IndentAndAppendLine(String(u"[Section start] Section index: ") + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitSectionEnd(SharedPtr<Section> section) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Section end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitBodyStart(SharedPtr<Body> body) override
    {
        int paragraphCount = body->get_Paragraphs()->get_Count();
        IndentAndAppendLine(String(u"[Body start] Paragraphs: ") + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitBodyEnd(SharedPtr<Body> body) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Body end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitParagraphStart(SharedPtr<Paragraph> paragraph) override
    {
        IndentAndAppendLine(u"[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitParagraphEnd(SharedPtr<Paragraph> paragraph) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Paragraph end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");

        return VisitorAction::Continue;
    }

    VisitorAction VisitSubDocument(SharedPtr<SubDocument> subDocument) override
    {
        IndentAndAppendLine(u"[SubDocument]");

        return VisitorAction::Continue;
    }

private:
    int mDocTraversalDepth;
    SharedPtr<System::Text::StringBuilder> mAcceptingNodeChildTree;

    void IndentAndAppendLine(String text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mAcceptingNodeChildTree->Append(u"|  ");
        }

        mAcceptingNodeChildTree->AppendLine(text);
    }
};
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
