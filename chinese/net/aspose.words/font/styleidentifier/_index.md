---
title: Font.StyleIdentifier
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置应用于此格式的字符样式的区域设置独立样式标识符
type: docs
weight: 410
url: /zh/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

获取或设置应用于此格式的字符样式的区域设置独立样式标识符。

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### 例子

演示如何更改现有文本的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种引用样式的方法。
// 1 - 使用样式名称：
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - 使用内置样式标识符：
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// 将一种样式的所有使用转换为另一种样式，
// 使用上述方法引用新旧样式。
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
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
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


