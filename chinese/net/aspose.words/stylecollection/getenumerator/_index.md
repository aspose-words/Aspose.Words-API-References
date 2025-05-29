---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: 探索 StyleCollection 的 GetEnumerator 方法，轻松按名称字母顺序列出样式。立即提升您的编码效率！
type: docs
weight: 90
url: /zh/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

获取一个枚举器对象，该对象将按照名称的字母顺序枚举样式。

```csharp
public IEnumerator<Style> GetEnumerator()
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

* class [Style](../../style/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
