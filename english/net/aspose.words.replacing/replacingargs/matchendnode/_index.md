---
title: ReplacingArgs.MatchEndNode
linktitle: MatchEndNode
articleTitle: MatchEndNode
second_title: Aspose.Words for .NET
description: ReplacingArgs MatchEndNode property guide. Access the ending node of text matches during document search and replace operations.
type: docs
weight: 40
url: /net/aspose.words.replacing/replacingargs/matchendnode/
---
## ReplacingArgs.MatchEndNode property

Gets the node that contains the end of the match.

```csharp
public Node MatchEndNode { get; }
```

## Examples

Shows how to get match end node.

```csharp
[Test]
public void MatchEndNode()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("1");
    builder.Writeln("2");
    builder.Writeln("3");

    ReplacingCallback replacingCallback = new ReplacingCallback();
    FindReplaceOptions opts = new FindReplaceOptions();
    opts.ReplacingCallback = replacingCallback;

    doc.Range.Replace(new Regex("1[\\s\\S]*3"), "X", opts);
    Assert.That(replacingCallback.StartNodeText, Is.EqualTo("1"));
    Assert.That(replacingCallback.EndNodeText, Is.EqualTo("3"));
}

/// <summary>
/// The replacing callback.
/// </summary>
private class ReplacingCallback : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        StartNodeText = e.MatchNode.GetText().Trim();
        EndNodeText = e.MatchEndNode.GetText().Trim();

        return ReplaceAction.Replace;
    }

    internal string StartNodeText { get; private set; }
    internal string EndNodeText { get; private set; }
}
```

### See Also

* class [Node](../../../aspose.words/node/)
* class [ReplacingArgs](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
