---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: 用于 .NET 的 Aspose.Words
description: Style BuiltIn 财产. 如果此样式是 MS Word 中的内置样式之一则为 True 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

如果此样式是 MS Word 中的内置样式之一，则为 True。

```csharp
public bool BuiltIn { get; }
```

## 例子

演示如何区分自定义样式和内置样式。

```csharp
Document doc = new Document();

// 当我们使用 Microsoft Word 创建文档或使用 Aspose.Words 以编程方式创建文档时，
// 该文档将附带一组样式，可应用于其文本以修改其外观。
// 我们可以通过文档的“Styles”集合访问这些内置样式。
// 这些样式都将“BuiltIn”标志设置为“true”。
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// 创建自定义样式并将其添加到集合中。
// 像这样的自定义样式会将“BuiltIn”标志设置为“false”。
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
