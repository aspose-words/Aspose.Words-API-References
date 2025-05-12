---
title: Run.getText method
linktitle: getText method
articleTitle: getText method
second_title: Aspose.Words for Node.js
description: "Run.getText method. Gets the text of the run."
type: docs
weight: 60
url: /nodejs-net/aspose.words/run/getText/
---

## getText() {#default}

Gets the text of the run.


```js
getText()
```

### Returns

The text of the run.


### Examples

Shows how to print the node structure of every header and footer in a document.

```js
test('HeaderFooterToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new HeaderFooterStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());

  // An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
  let headerFooters = doc.firstSection.headersFooters.toArray();
  expect(headerFooters.length).toEqual(3);
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered HeaderFooter nodes and their children.
  /// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
  public HeaderFooterStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideHeaderFooter = false;
  }

  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a HeaderFooter node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
  {
    IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.headerFooterType);
    mDocTraversalDepth++;
    mVisitorIsInsideHeaderFooter = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a HeaderFooter node have been visited.
    /// </summary>
  public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[HeaderFooter end]");
    mVisitorIsInsideHeaderFooter = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++) mBuilder.append("|  ");

    mBuilder.AppendLine(text);
  }

  private bool mVisitorIsInsideHeaderFooter;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words](../../)
* class [Run](../)

