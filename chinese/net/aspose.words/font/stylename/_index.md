---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: 用于 .NET 的 Aspose.Words
description: Font StyleName 财产. 获取或设置应用于此格式的字符样式的名称 在 C#.
type: docs
weight: 420
url: /zh/net/aspose.words/font/stylename/
---
## Font.StyleName property

获取或设置应用于此格式的字符样式的名称。

```csharp
public string StyleName { get; set; }
```

## 例子

显示如何更改现有文本的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是引用样式的两种方式。
// 1 - 使用样式名称：
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - 使用内置样式标识符：
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// 将一种样式的所有用途转换为另一种样式，
// 使用上述方法来引用新旧样式。
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

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
