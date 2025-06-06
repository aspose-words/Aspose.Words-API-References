---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words FindReplaceDirection 枚举，实现高效的文本替换。通过精确的方向控制优化您的文档处理。
type: docs
weight: 5340
url: /zh/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

指定替换操作的方向。

```csharp
public enum FindReplaceDirection
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Forward | `0` | 匹配的项目将从第一个到最后一个进行替换。 |
| Backward | `1` | 匹配的项目将从最后一个替换为第一个。 |

## 例子

展示如何确定查找和替换操作遍历文档的方向。

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入三个我们可以使用正则表达式模式进行搜索的运行。
    // 将其中一个运行放在文本框内。
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();

    // 将自定义回调分配给“ReplacingCallback”属性。
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // 将“Direction”属性设置为“FindReplaceDirection.Backward”以获取查找和替换
    // 操作从范围的末尾开始，然后遍历回开头。
    // 将“Direction”属性设置为“FindReplaceDirection.Forward”以获取查找和替换
    // 操作从范围的开头开始，遍历到结尾。
    options.Direction = findReplaceDirection;

    doc.Range.Replace(new Regex(@"Match \d*"), "Replacement", options);

    Assert.AreEqual("Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.", doc.GetText().Trim());

    switch (findReplaceDirection)
    {
        case FindReplaceDirection.Forward:
            Assert.AreEqual(new[] { "Match 1", "Match 2", "Match 3", "Match 4" }, callback.Matches);
            break;
        case FindReplaceDirection.Backward:
            Assert.AreEqual(new[] { "Match 4", "Match 3", "Match 2", "Match 1" }, callback.Matches);
            break;
    }
}

/// <summary>
/// 按照发生的顺序记录查找和替换操作期间发生的所有匹配。
/// </summary>
private class TextReplacementRecorder : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Replacing](../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../)
