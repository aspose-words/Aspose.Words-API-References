---
title: VisitorAction enumeration
linktitle: VisitorAction enumeration
articleTitle: VisitorAction enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.VisitorAction enumeration. Allows the visitor to control the enumeration of nodes."
type: docs
weight: 1450
url: /nodejs-net/aspose.words/visitoraction/
---

## VisitorAction enumeration

Allows the visitor to control the enumeration of nodes.


### Members

| Name | Description |
| --- | --- |
| Continue | The visitor requests the enumeration to continue. |
| SkipThisNode | The visitor requests to skip the current node and continue enumeration. |
| Stop | The visitor requests the enumeration of nodes to stop. |

### Examples

Shows how to process absolute position tab characters with a document visitor.

```js
test('DocumentToTxt', () => {
  let doc = new aw.Document(base.myDir + "Absolute position tab.docx");

  // Extract the text contents of our document by accepting this custom document visitor.
  let myDocTextExtractor = new DocTextExtractor();
  let fisrtSection = doc.firstSection;
  fisrtSection.body.accept(myDocTextExtractor);
  // Visit only start of the document body.
  fisrtSection.body.acceptStart(myDocTextExtractor);
  // Visit only end of the document body.
  fisrtSection.body.acceptEnd(myDocTextExtractor);

  // The absolute position tab, which has no equivalent in string form, has been explicitly converted to a tab character.
  expect(myDocTextExtractor.getText()).toEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab");

  // An AbsolutePositionTab can accept a DocumentVisitor by itself too.
  let absPositionTab = (AbsolutePositionTab)doc.firstSection.body.firstParagraph.getChild(aw.NodeType.SpecialChar, 0, true);

  myDocTextExtractor = new DocTextExtractor();
  absPositionTab.accept(myDocTextExtractor);

  expect(myDocTextExtractor.getText()).toEqual("\t");
});


  /// <summary>
  /// Collects the text contents of all runs in the visited document. Replaces all absolute tab characters with ordinary tabs.
  /// </summary>
public class DocTextExtractor : DocumentVisitor
{
  public DocTextExtractor()
  {
    mBuilder = new StringBuilder();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    AppendText(run.text);
    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when an AbsolutePositionTab node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
  {
    mBuilder.append("\t");
    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Adds text to the current output. Honors the enabled/disabled output flag.
    /// </summary>
  private void AppendText(string text)
  {
    mBuilder.append(text);
  }

    /// <summary>
    /// Plain text of the document that was accumulated by the visitor.
    /// </summary>
  public string GetText()
  {
    return mBuilder.toString();
  }

  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words](../)

