---
title: ReplaceAction Enum
linktitle: ReplaceAction
articleTitle: ReplaceAction
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Replacing.ReplaceAction 枚举. 允许用户指定在替换操作期间当前匹配会发生什么情况 在 C#.
type: docs
weight: 4640
url: /zh/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

允许用户指定在替换操作期间当前匹配会发生什么情况。

```csharp
public enum ReplaceAction
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Replace | `0` | 替换当前匹配项。 |
| Skip | `1` | 跳过当前匹配。 |
| Stop | `2` | 终止替换操作。 |

## 例子

演示如何在查找和替换操作中插入整个文档的内容作为匹配项的替换。

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // 在包含匹配文本的段落之后插入文档。
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // 删除具有匹配文本的段落。
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
                // 如果该节点是节中最后一个空段落，则跳过该节点。
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
