---
title: ReplacingArgs.MatchOffset
linktitle: MatchOffset
articleTitle: MatchOffset
second_title: Aspose.Words for .NET
description: 发现 ReplacingArgs MatchOffset 属性，轻松找到节点中匹配的从零开始的起始位置，以实现高效的数据处理。
type: docs
weight: 50
url: /zh/net/aspose.words.replacing/replacingargs/matchoffset/
---
## ReplacingArgs.MatchOffset property

从包含匹配开头的节点的开始处获取匹配的从零开始的起始位置。

```csharp
public int MatchOffset { get; }
```

## 例子

展示如何通过 FindReplaceOptions 将不同的字体应用于新内容。

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();

    // 将“HighlightColor”属性设置为我们想要应用于操作的结果文本的背景颜色。
    options.ApplyFont.HighlightColor = Color.LightGray;

    NumberHexer numberHexer = new NumberHexer();
    options.ReplacingCallback = numberHexer;

    int replacementCount = doc.Range.Replace(new Regex("[0-9]+"), "", options);

    Console.WriteLine(numberHexer.GetLog());

    Assert.AreEqual(4, replacementCount);
    Assert.AreEqual("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
                    "0x7B, 0x1C8, 0x315 and 0x43E3.", doc.GetText().Trim());
    Assert.AreEqual(4, doc.GetChildNodes(NodeType.Run, true).OfType<Run>()
            .Count(r => r.Font.HighlightColor.ToArgb() == Color.LightGray.ToArgb()));
}

/// <summary>
/// 用十六进制等效值替换数字查找和替换匹配项。
/// 维护每次替换的日志。
/// </summary>
private class NumberHexer : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mCurrentReplacementNumber++;

        int number = Convert.ToInt32(args.Match.Value);

        args.Replacement = $"0x{number:X}";

        mLog.AppendLine($"Match #{mCurrentReplacementNumber}");
        mLog.AppendLine($"\tOriginal value:\t{args.Match.Value}");
        mLog.AppendLine($"\tReplacement:\t{args.Replacement}");
        mLog.AppendLine($"\tOffset in parent {args.MatchNode.NodeType} node:\t{args.MatchOffset}");

        mLog.AppendLine(string.IsNullOrEmpty(args.GroupName)
            ? $"\tGroup index:\t{args.GroupIndex}"
            : $"\tGroup name:\t{args.GroupName}");

        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private int mCurrentReplacementNumber;
    private readonly StringBuilder mLog = new StringBuilder();
}
```

### 也可以看看

* class [ReplacingArgs](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
