---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words for .NET
description: 了解某种样式是否是 MS Word 的内置选项。使用我们全面的 Word 内置样式指南，提升您的文档设计！
type: docs
weight: 40
url: /zh/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

如果此样式是 MS Word 中的内置样式之一，则为真。

```csharp
public bool BuiltIn { get; }
```

## 例子

展示如何区分自定义样式和内置样式。

```csharp
Document doc = new Document();

// 当我们使用 Microsoft Word 或以编程方式使用 Aspose.Words 创建文档时，
// 该文档将附带一组样式，可应用于其文本以修改其外观。
// 我们可以通过文档的“样式”集合访问这些内置样式。
// 这些样式都将“BuiltIn”标志设置为“true”。
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// 创建自定义样式并将其添加到集合中。
 // 此类自定义样式将把“BuiltIn”标志设置为“false”。
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
