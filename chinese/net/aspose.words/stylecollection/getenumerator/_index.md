---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: 用于 .NET 的 Aspose.Words
description: StyleCollection GetEnumerator 方法. 获取一个枚举器对象该对象将按名称的字母顺序枚举样式 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

获取一个枚举器对象，该对象将按名称的字母顺序枚举样式。

```csharp
public IEnumerator<Style> GetEnumerator()
```

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

* class [Style](../../style/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
