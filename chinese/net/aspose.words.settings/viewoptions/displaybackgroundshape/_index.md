---
title: ViewOptions.DisplayBackgroundShape
second_title: Aspose.Words for .NET API 参考
description: ViewOptions 财产. 控制打印布局视图中背景形状的显示
type: docs
weight: 10
url: /zh/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

控制打印布局视图中背景形状的显示。

```csharp
public bool DisplayBackgroundShape { get; set; }
```

### 例子

演示如何在视图选项中隐藏/显示文档背景图像。

```csharp
// 使用 HTML 字符串创建一个具有平坦背景颜色的新文档。
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// 文档的源具有平坦的彩色背景，
// 其存在会将“DisplayBackgroundShape”标志设置为“true”。
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// 将“DisplayBackgroundShape”保留为“true”以使文档显示背景颜色。
// 这可能会影响一些文本颜色以提高可见性。
// 将“DisplayBackgroundShape”设置为“false”以不显示背景颜色。
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### 也可以看看

* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../viewoptions/)
* 部件 [Aspose.Words](../../../)


