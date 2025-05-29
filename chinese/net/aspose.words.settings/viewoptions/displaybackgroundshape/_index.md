---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words for .NET
description: 探索 ViewOptions 中的 DisplayBackgroundShape 属性，使用可自定义的背景形状增强打印布局，获得更精致的外观。
type: docs
weight: 10
url: /zh/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

控制打印布局视图中背景形状的显示。

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## 例子

显示如何在视图选项中隐藏/显示文档背景图像。

```csharp
// 使用 HTML 字符串创建具有平面背景颜色的新文档。
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// 文档源具有纯色背景，
// 其存在将把“DisplayBackgroundShape”标志设置为“true”。
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// 保持“DisplayBackgroundShape”为“true”以使文档显示背景颜色。
// 这可能会影响某些文本颜色以提高可见性。
// 将“DisplayBackgroundShape”设置为“false”以不显示背景颜色。
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### 也可以看看

* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
