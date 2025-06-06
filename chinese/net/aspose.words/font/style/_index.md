---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: 了解如何使用字体样式属性自定义格式中的字符样式，以增强文本的吸引力和可读性。
type: docs
weight: 410
url: /zh/net/aspose.words/font/style/
---
## Font.Style property

获取或设置应用于此格式的字符样式。

```csharp
public Style Style { get; set; }
```

## 例子

对文档中所有使用自定义字符样式格式化的运行应用双下划线。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入自定义样式并将其应用于使用文档构建器创建的文本。
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// 遍历每次运行并为每个自定义样式添加双下划线。
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### 也可以看看

* class [Style](../../style/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
