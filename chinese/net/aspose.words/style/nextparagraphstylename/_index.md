---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: 用于 .NET 的 Aspose.Words
description: Style NextParagraphStyleName 财产. 获取/设置要自动应用于在使用指定样式格式化的 a 段落之后插入的新段落的样式名称 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

获取/设置要自动应用于在使用指定样式格式化的 a 段落之后插入的新段落的样式名称。

```csharp
public string NextParagraphStyleName { get; set; }
```

## 评论

Aspose.Words 不使用此属性。当您在 MS Word 中编辑文档时，只会自动应用下一个段落样式。 。

## 例子

演示如何访问文档的样式集合。

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// 枚举并列出使用 Aspose.Words 创建的文档默认包含的所有样式。
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
