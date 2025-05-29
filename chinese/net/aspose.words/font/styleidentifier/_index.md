---
title: Font.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words for .NET
description: 探索 Font StyleIdentifier 属性，轻松管理格式中的字符样式。使用独立于语言环境的解决方案增强您的设计！
type: docs
weight: 420
url: /zh/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

获取或设置应用于此格式的字符样式的区域设置独立样式标识符。

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## 例子

展示如何改变现有文本的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种引用样式的方式。
// 1 - 使用样式名称：
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - 使用内置样式标识符：
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// 将一种风格的所有用途转换为另一种风格，
// 使用上述方法引用新旧样式。
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### 也可以看看

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
