---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words for .NET
description: 了解如何有效地使用 NextParagraphStyleName 属性来自动化新段落的样式应用，从而增强文档格式。
type: docs
weight: 140
url: /zh/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

获取/设置自动应用于在用指定样式格式化的段落后插入的新段落的样式名称。

```csharp
public string NextParagraphStyleName { get; set; }
```

## 评论

Aspose.Words 不使用此属性。只有当您在 MS Word 中编辑文档时，才会自动应用下一个段落样式。

## 例子

展示如何访问文档的样式集合。

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
