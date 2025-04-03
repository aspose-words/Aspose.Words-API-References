---
title: DocumentVisitor.visitSectionEnd method
linktitle: visitSectionEnd method
articleTitle: visitSectionEnd method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitSectionEnd method. Called when enumeration of a section has ended."
type: docs
weight: 370
url: /nodejs-net/aspose.words/documentvisitor/visitSectionEnd/
---

## visitSectionEnd(section) {#section}

Called when enumeration of a section has ended.


```js
visitSectionEnd(section: Aspose.Words.Section)
```

| Parameter | Type | Description |
| --- | --- | --- |
| section | [Section](../../section/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


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

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

