---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 中的 UseLegacyOrder 属性。启用顺序文本搜索以提高准确性。默认值为 false。优化您的文本处理！
type: docs
weight: 180
url: /zh/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True 表示考虑文本框，按从上到下的顺序执行文本搜索。 默认值为`错误的`.

```csharp
public bool UseLegacyOrder { get; set; }
```

## 例子

展示如何在执行查找和替换文本操作时更改节点的搜索顺序。

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入三个我们可以使用正则表达式模式进行搜索的运行。
    // 将其中一个运行放在文本框内。
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();

    // 将自定义回调分配给“ReplacingCallback”属性。
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // 如果我们将“UseLegacyOrder”属性设置为“true”，则
    // 查找和替换操作将遍历文本框之外的所有运行
    // 在浏览文本框内的内容之前。
    // 如果我们将“UseLegacyOrder”属性设置为“false”，则
    // 查找和替换操作将按顺序遍历范围内的所有运行。
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// 记录查找和替换操作期间发生的所有匹配的顺序。
/// </summary>
private class TextReplacementTracker : IReplacingCallback
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

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
