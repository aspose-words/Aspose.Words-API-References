---
title: ReplacingArgs
second_title: Aspose.Words for .NET API 参考
description: 为自定义替换操作提供数据
type: docs
weight: 4390
url: /zh/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

为自定义替换操作提供数据。

```csharp
public class ReplacingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | 按索引标识在[`Match`](./match/) 被替换为[`Replacement`](./replacement/)字符串. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | 按名称标识在[`Match`](./match/) 被替换为[`Replacement`](./replacement/)字符串. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | 的Match由单个 regular 表达式匹配产生的 **代替**. |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | 获取包含匹配开头的节点。 |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | 从包含匹配开头的 节点的开头获取匹配的从零开始的位置。 |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | 获取或设置替换字符串。 |

### 例子

展示如何用另一个字符串替换所有出现的正则表达式模式，同时跟踪所有此类替换。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();

    // 设置一个回调来跟踪“替换”方法将进行的任何替换。
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// 维护由查找和替换操作完成的每个文本替换的日志
/// 并注意原始匹配文本的值。
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

演示如何在查找和替换操作中插入整个文档的内容以替换匹配项。

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // 在包含匹配文本的段落之后插入一个文档。
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // 删除匹配文本的段落。
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// 在段落或表格之后插入另一个文档的所有节点。
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // 如果节点是节中的最后一个空段落，则跳过该节点。
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### 也可以看看

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* 命名空间 [Aspose.Words.Replacing](../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
