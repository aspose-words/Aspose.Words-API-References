---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words for .NET
description: Explore Aspose.Words.VisitorAction enum to effortlessly manage node enumeration, enhancing your document processing efficiency and control.
type: docs
weight: 7500
url: /net/aspose.words/visitoraction/
---
## VisitorAction enumeration

Allows the visitor to control the enumeration of nodes.

```csharp
public enum VisitorAction
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Continue | `0` | The visitor requests the enumeration to continue. |
| SkipThisNode | `1` | The visitor requests to skip the current node and continue enumeration. |
| Stop | `2` | The visitor requests the enumeration of nodes to stop. |

## Examples

Shows how to process absolute position tab characters with a document visitor.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extract the text contents of our document by accepting this custom document visitor.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Visit only start of the document body.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Visit only end of the document body.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // The absolute position tab, which has no equivalent in string form, has been explicitly converted to a tab character.
    Assert.That(myDocTextExtractor.GetText(), Is.EqualTo("Before AbsolutePositionTab\tAfter AbsolutePositionTab"));

    // An AbsolutePositionTab can accept a DocumentVisitor by itself too.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.That(myDocTextExtractor.GetText(), Is.EqualTo("\t"));
}

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
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when an AbsolutePositionTab node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Adds text to the current output. Honors the enabled/disabled output flag.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Plain text of the document that was accumulated by the visitor.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
