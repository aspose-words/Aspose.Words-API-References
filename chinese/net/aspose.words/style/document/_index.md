---
title: Style.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 发现样式文档属性，轻松访问和管理您的所有者文档，从而增强组织性和效率。
type: docs
weight: 50
url: /zh/net/aspose.words/style/document/
---
## Style.Document property

获取所有者文档。

```csharp
public DocumentBase Document { get; }
```

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

* class [DocumentBase](../../documentbase/)
* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
