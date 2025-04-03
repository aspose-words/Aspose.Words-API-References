---
title: DocumentVisitor class
linktitle: DocumentVisitor class
articleTitle: DocumentVisitor class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentVisitor class. Base class for custom document visitors"
type: docs
weight: 350
url: /nodejs-net/aspose.words/documentvisitor/
---

## DocumentVisitor class

Base class for custom document visitors.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

With [DocumentVisitor](./) you can define and execute custom operations
that require enumeration over the document tree.

For example, Aspose.Words uses [DocumentVisitor](./) internally for saving [Document](../document/)
in various formats and for other operations like finding fields or bookmarks over
a fragment of a document.

To use [DocumentVisitor](./):


1. Create a class derived from [DocumentVisitor](./).
   
1. Override and provide implementations for some or all of the VisitXXX methods
   to perform some custom operations.
   
1. Call [Node.accept()](../node/accept/#documentvisitor) on the [Node](../node/) that
   you want to start the enumeration from.
   
[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods 
to make it easier to create new document visitors as only the methods required for the particular
visitor need to be overridden. It is not necessary to override all of the visitor methods.

For more information see the Visitor design pattern.




### Methods

| Name | Description |
| --- | --- |
|[ visitAbsolutePositionTab(tab)](./visitAbsolutePositionTab/#absolutepositiontab) | Called when a [AbsolutePositionTab](../absolutepositiontab/) node is encountered in the document. |
|[ visitBodyEnd(body)](./visitBodyEnd/#body) | Called when enumeration of the main text story in a section has ended. |
|[ visitBodyStart(body)](./visitBodyStart/#body) | Called when enumeration of the main text story in a section has started. |
|[ visitBookmarkEnd(bookmarkEnd)](./visitBookmarkEnd/#bookmarkend) | Called when an end of a bookmark is encountered in the document. |
|[ visitBookmarkStart(bookmarkStart)](./visitBookmarkStart/#bookmarkstart) | Called when a start of a bookmark is encountered in the document. |
|[ visitBuildingBlockEnd(block)](./visitBuildingBlockEnd/#buildingblock) | Called when enumeration of a building block has ended. |
|[ visitBuildingBlockStart(block)](./visitBuildingBlockStart/#buildingblock) | Called when enumeration of a building block has started. |
|[ visitCellEnd(cell)](./visitCellEnd/#cell) | Called when enumeration of a table cell has ended. |
|[ visitCellStart(cell)](./visitCellStart/#cell) | Called when enumeration of a table cell has started. |
|[ visitCommentEnd(comment)](./visitCommentEnd/#comment) | Called when enumeration of a comment text has ended. |
|[ visitCommentRangeEnd(commentRangeEnd)](./visitCommentRangeEnd/#commentrangeend) | Called when the end of a commented range of text is encountered. |
|[ visitCommentRangeStart(commentRangeStart)](./visitCommentRangeStart/#commentrangestart) | Called when the start of a commented range of text is encountered. |
|[ visitCommentStart(comment)](./visitCommentStart/#comment) | Called when enumeration of a comment text has started. |
|[ visitDocumentEnd(doc)](./visitDocumentEnd/#document) | Called when enumeration of the document has finished. |
|[ visitDocumentStart(doc)](./visitDocumentStart/#document) | Called when enumeration of the document has started. |
|[ visitEditableRangeEnd(editableRangeEnd)](./visitEditableRangeEnd/#editablerangeend) | Called when an end of an editable range is encountered in the document. |
|[ visitEditableRangeStart(editableRangeStart)](./visitEditableRangeStart/#editablerangestart) | Called when a start of an editable range is encountered in the document. |
|[ visitFieldEnd(fieldEnd)](./visitFieldEnd/#fieldend) | Called when a field ends in the document. |
|[ visitFieldSeparator(fieldSeparator)](./visitFieldSeparator/#fieldseparator) | Called when a field separator is encountered in the document. |
|[ visitFieldStart(fieldStart)](./visitFieldStart/#fieldstart) | Called when a field starts in the document. |
|[ visitFootnoteEnd(footnote)](./visitFootnoteEnd/#footnote) | Called when enumeration of a footnote or endnote text has ended. |
|[ visitFootnoteStart(footnote)](./visitFootnoteStart/#footnote) | Called when enumeration of a footnote or endnote text has started. |
|[ visitFormField(formField)](./visitFormField/#formfield) | Called when a form field is encountered in the document. |
|[ visitGlossaryDocumentEnd(glossary)](./visitGlossaryDocumentEnd/#glossarydocument) | Called when enumeration of a glossary document has ended. |
|[ visitGlossaryDocumentStart(glossary)](./visitGlossaryDocumentStart/#glossarydocument) | Called when enumeration of a glossary document has started. |
|[ visitGroupShapeEnd(groupShape)](./visitGroupShapeEnd/#groupshape) | Called when enumeration of a group shape has ended. |
|[ visitGroupShapeStart(groupShape)](./visitGroupShapeStart/#groupshape) | Called when enumeration of a group shape has started. |
|[ visitHeaderFooterEnd(headerFooter)](./visitHeaderFooterEnd/#headerfooter) | Called when enumeration of a header or footer in a section has ended. |
|[ visitHeaderFooterStart(headerFooter)](./visitHeaderFooterStart/#headerfooter) | Called when enumeration of a header or footer in a section has started. |
|[ visitOfficeMathEnd(officeMath)](./visitOfficeMathEnd/#officemath) | Called when enumeration of a Office Math object has ended. |
|[ visitOfficeMathStart(officeMath)](./visitOfficeMathStart/#officemath) | Called when enumeration of a Office Math object has started. |
|[ visitParagraphEnd(paragraph)](./visitParagraphEnd/#paragraph) | Called when enumeration of a paragraph has ended. |
|[ visitParagraphStart(paragraph)](./visitParagraphStart/#paragraph) | Called when enumeration of a paragraph has started. |
|[ visitRowEnd(row)](./visitRowEnd/#row) | Called when enumeration of a table row has ended. |
|[ visitRowStart(row)](./visitRowStart/#row) | Called when enumeration of a table row has started. |
|[ visitRun(run)](./visitRun/#run) | Called when a run of text in the is encountered. |
|[ visitSectionEnd(section)](./visitSectionEnd/#section) | Called when enumeration of a section has ended. |
|[ visitSectionStart(section)](./visitSectionStart/#section) | Called when enumeration of a section has started. |
|[ visitShapeEnd(shape)](./visitShapeEnd/#shape) | Called when enumeration of a shape has ended. |
|[ visitShapeStart(shape)](./visitShapeStart/#shape) | Called when enumeration of a shape has started. |
|[ visitSmartTagEnd(smartTag)](./visitSmartTagEnd/#smarttag) | Called when enumeration of a smart tag has ended. |
|[ visitSmartTagStart(smartTag)](./visitSmartTagStart/#smarttag) | Called when enumeration of a smart tag has started. |
|[ visitSpecialChar(specialChar)](./visitSpecialChar/#specialchar) | Called when a [SpecialChar](../specialchar/) node is encountered in the document. |
|[ visitStructuredDocumentTagEnd(sdt)](./visitStructuredDocumentTagEnd/#structureddocumenttag) | Called when enumeration of a structured document tag has ended. |
|[ visitStructuredDocumentTagRangeEnd(sdtRangeEnd)](./visitStructuredDocumentTagRangeEnd/#structureddocumenttagrangeend) | Called when a StructuredDocumentTagRangeEnd is encountered. |
|[ visitStructuredDocumentTagRangeStart(sdtRangeStart)](./visitStructuredDocumentTagRangeStart/#structureddocumenttagrangestart) | Called when a StructuredDocumentTagRangeStart is encountered. |
|[ visitStructuredDocumentTagStart(sdt)](./visitStructuredDocumentTagStart/#structureddocumenttag) | Called when enumeration of a structured document tag has started. |
|[ visitSubDocument(subDocument)](./visitSubDocument/#subdocument) | Called when a sub-document is encountered. |
|[ visitTableEnd(table)](./visitTableEnd/#table) | Called when enumeration of a table has ended. |
|[ visitTableStart(table)](./visitTableStart/#table) | Called when enumeration of a table has started. |

### Examples

Shows how to use a document visitor to print a document's node structure.

```js
test('DocStructureToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new DocStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


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
    return mAcceptingNodeChildTree.toString();
  }

    /// <summary>
    /// Called when a Document node is encountered.
    /// </summary>
  public override VisitorAction VisitDocumentStart(Document doc)
  {
    int childNodeCount = doc.getChildNodes(aw.NodeType.Any, true).Count;

    IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
    mDocTraversalDepth++;

      // Allow the visitor to continue visiting other nodes.
    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Document node have been visited.
    /// </summary>
  public override VisitorAction VisitDocumentEnd(Document doc)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Document end]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Section node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitSectionStart(Section section)
  {
      // Get the index of our section within the document.
    let docSections = section.document.getChildNodes(aw.NodeType.Section, false);
    int sectionIndex = docSections.indexOf(section);

    IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
    mDocTraversalDepth++;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Section node have been visited.
    /// </summary>
  public override VisitorAction VisitSectionEnd(Section section)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Section end]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Body node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitBodyStart(Body body)
  {
    int paragraphCount = body.paragraphs.count;
    IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
    mDocTraversalDepth++;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Body node have been visited.
    /// </summary>
  public override VisitorAction VisitBodyEnd(Body body)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Body end]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Paragraph node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitParagraphStart(Paragraph paragraph)
  {
    IndentAndAppendLine("[Paragraph start]");
    mDocTraversalDepth++;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Paragraph node have been visited.
    /// </summary>
  public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Paragraph end]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a SubDocument node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitSubDocument(SubDocument subDocument)
  {
    IndentAndAppendLine("[SubDocument]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.append("|  ");

    mAcceptingNodeChildTree.AppendLine(text);
  }

  private int mDocTraversalDepth;
  private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### See Also

* module [Aspose.Words](../)

