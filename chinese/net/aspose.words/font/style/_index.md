---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: 用于 .NET 的 Aspose.Words
description: Font Style 财产. 获取或设置应用于此格式的字符样式 在 C#.
type: docs
weight: 400
url: /zh/net/aspose.words/font/style/
---
## Font.Style property

获取或设置应用于此格式的字符样式。

```csharp
public Style Style { get; set; }
```

## 例子

对文档中使用自定义字符样式格式化的所有运行应用双下划线。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入自定义样式并将其应用到使用文档生成器创建的文本。
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// 迭代每次运行并向每个自定义样式添加双下划线。
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
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
