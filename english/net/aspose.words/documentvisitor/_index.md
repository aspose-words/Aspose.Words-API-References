---
title: DocumentVisitor
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 450
url: /net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Base class for custom document visitors.

```csharp
public abstract class DocumentVisitor
```

## Methods

| Name | Description |
| --- | --- |
| virtual [VisitAbsolutePositionTab](visitabsolutepositiontab)(AbsolutePositionTab) | Called when a [`AbsolutePositionTab`](../absolutepositiontab) node is encountered in the document. |
| virtual [VisitBodyEnd](visitbodyend)(Body) | Called when enumeration of the main text story in a section has ended. |
| virtual [VisitBodyStart](visitbodystart)(Body) | Called when enumeration of the main text story in a section has started. |
| virtual [VisitBookmarkEnd](visitbookmarkend)(BookmarkEnd) | Called when an end of a bookmark is encountered in the document. |
| virtual [VisitBookmarkStart](visitbookmarkstart)(BookmarkStart) | Called when a start of a bookmark is encountered in the document. |
| virtual [VisitBuildingBlockEnd](visitbuildingblockend)(BuildingBlock) | Called when enumeration of a building block has ended. |
| virtual [VisitBuildingBlockStart](visitbuildingblockstart)(BuildingBlock) | Called when enumeration of a building block has started. |
| virtual [VisitCellEnd](visitcellend)(Cell) | Called when enumeration of a table cell has ended. |
| virtual [VisitCellStart](visitcellstart)(Cell) | Called when enumeration of a table cell has started. |
| virtual [VisitCommentEnd](visitcommentend)(Comment) | Called when enumeration of a comment text has ended. |
| virtual [VisitCommentRangeEnd](visitcommentrangeend)(CommentRangeEnd) | Called when the end of a commented range of text is encountered. |
| virtual [VisitCommentRangeStart](visitcommentrangestart)(CommentRangeStart) | Called when the start of a commented range of text is encountered. |
| virtual [VisitCommentStart](visitcommentstart)(Comment) | Called when enumeration of a comment text has started. |
| virtual [VisitDocumentEnd](visitdocumentend)(Document) | Called when enumeration of the document has finished. |
| virtual [VisitDocumentStart](visitdocumentstart)(Document) | Called when enumeration of the document has started. |
| virtual [VisitEditableRangeEnd](visiteditablerangeend)(EditableRangeEnd) | Called when an end of an editable range is encountered in the document. |
| virtual [VisitEditableRangeStart](visiteditablerangestart)(EditableRangeStart) | Called when a start of an editable range is encountered in the document. |
| virtual [VisitFieldEnd](visitfieldend)(FieldEnd) | Called when a field ends in the document. |
| virtual [VisitFieldSeparator](visitfieldseparator)(FieldSeparator) | Called when a field separator is encountered in the document. |
| virtual [VisitFieldStart](visitfieldstart)(FieldStart) | Called when a field starts in the document. |
| virtual [VisitFootnoteEnd](visitfootnoteend)(Footnote) | Called when enumeration of a footnote or endnote text has ended. |
| virtual [VisitFootnoteStart](visitfootnotestart)(Footnote) | Called when enumeration of a footnote or endnote text has started. |
| virtual [VisitFormField](visitformfield)(FormField) | Called when a form field is encountered in the document. |
| virtual [VisitGlossaryDocumentEnd](visitglossarydocumentend)(GlossaryDocument) | Called when enumeration of a glossary document has ended. |
| virtual [VisitGlossaryDocumentStart](visitglossarydocumentstart)(GlossaryDocument) | Called when enumeration of a glossary document has started. |
| virtual [VisitGroupShapeEnd](visitgroupshapeend)(GroupShape) | Called when enumeration of a group shape has ended. |
| virtual [VisitGroupShapeStart](visitgroupshapestart)(GroupShape) | Called when enumeration of a group shape has started. |
| virtual [VisitHeaderFooterEnd](visitheaderfooterend)(HeaderFooter) | Called when enumeration of a header or footer in a section has ended. |
| virtual [VisitHeaderFooterStart](visitheaderfooterstart)(HeaderFooter) | Called when enumeration of a header or footer in a section has started. |
| virtual [VisitOfficeMathEnd](visitofficemathend)(OfficeMath) | Called when enumeration of a Office Math object has ended. |
| virtual [VisitOfficeMathStart](visitofficemathstart)(OfficeMath) | Called when enumeration of a Office Math object has started. |
| virtual [VisitParagraphEnd](visitparagraphend)(Paragraph) | Called when enumeration of a paragraph has ended. |
| virtual [VisitParagraphStart](visitparagraphstart)(Paragraph) | Called when enumeration of a paragraph has started. |
| virtual [VisitRowEnd](visitrowend)(Row) | Called when enumeration of a table row has ended. |
| virtual [VisitRowStart](visitrowstart)(Row) | Called when enumeration of a table row has started. |
| virtual [VisitRun](visitrun)(Run) | Called when a run of text in the is encountered. |
| virtual [VisitSectionEnd](visitsectionend)(Section) | Called when enumeration of a section has ended. |
| virtual [VisitSectionStart](visitsectionstart)(Section) | Called when enumeration of a section has started. |
| virtual [VisitShapeEnd](visitshapeend)(Shape) | Called when enumeration of a shape has ended. |
| virtual [VisitShapeStart](visitshapestart)(Shape) | Called when enumeration of a shape has started. |
| virtual [VisitSmartTagEnd](visitsmarttagend)(SmartTag) | Called when enumeration of a smart tag has ended. |
| virtual [VisitSmartTagStart](visitsmarttagstart)(SmartTag) | Called when enumeration of a smart tag has started. |
| virtual [VisitSpecialChar](visitspecialchar)(SpecialChar) | Called when a [`SpecialChar`](../specialchar) node is encountered in the document. |
| virtual [VisitStructuredDocumentTagEnd](visitstructureddocumenttagend)(StructuredDocumentTag) | Called when enumeration of a structured document tag has ended. |
| virtual [VisitStructuredDocumentTagRangeEnd](visitstructureddocumenttagrangeend)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](visitstructureddocumenttagrangestart)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](visitstructureddocumenttagstart)(StructuredDocumentTag) | Called when enumeration of a structured document tag has started. |
| virtual [VisitSubDocument](visitsubdocument)(SubDocument) | Called when a subDocument is encountered. |
| virtual [VisitTableEnd](visittableend)(Table) | Called when enumeration of a table has ended. |
| virtual [VisitTableStart](visittablestart)(Table) | Called when enumeration of a table has started. |

### Remarks

With **DocumentVisitor** you can define and execute custom operations that require enumeration over the document tree.

For example, Aspose.Words uses **DocumentVisitor** internally for saving **Document** in various formats and for other operations like finding fields or bookmarks over a fragment of a document.

To use **DocumentVisitor**:

1. Create a class derived from **DocumentVisitor**.
2. Override and provide implementations for some or all of the VisitXXX methods to perform some custom operations.
3. Call [`Node.Accept`](../node/accept) on the **Node** that you want to start the enumeration from.

**DocumentVisitor** provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

For more information see the Visitor design pattern.

### Examples

Shows how to use a document visitor to print a document's node structure.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Traverses a node's tree of child nodes.
/// Creates a map of this tree in the form of a string.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Called when a Document node is encountered.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Allow the visitor to continue visiting other nodes.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called after all the child nodes of a Document node have been visited.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Section node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Get the index of our section within the document.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called after all the child nodes of a Section node have been visited.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Body node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called after all the child nodes of a Body node have been visited.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Paragraph node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called after all the child nodes of a Paragraph node have been visited.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a SubDocument node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### See Also

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
