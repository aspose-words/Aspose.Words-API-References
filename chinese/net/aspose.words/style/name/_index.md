---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: 发现样式名称属性，轻松管理和自定义您的样式，以增强设计灵活性和用户体验。
type: docs
weight: 130
url: /zh/net/aspose.words/style/name/
---
## Style.Name property

获取或设置样式的名称。

```csharp
public string Name { get; set; }
```

## 评论

不能为空字符串。

如果集合中已存在同名样式，则新样式将覆盖原样式。所有受影响的节点都将引用新样式。

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

展示如何克隆文档的样式。

```csharp
Document doc = new Document();

// AddCopy 方法创建指定样式的副本，并且
// 自动为样式生成一个新名称，例如“Heading 1_0”。
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// 使用样式的“名称”属性来更改样式的识别名称。
newStyle.Name = "My Heading 1";

// 我们的文档现在有两种外观相同但名称不同的样式。
// 更改其中一种样式的设置不会影响另一种样式。
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
