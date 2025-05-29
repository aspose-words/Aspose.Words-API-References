---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words for .NET
description: 发现 ShapeBase ScreenTip 属性，通过自定义鼠标悬停在形状上时显示的工具提示文本来增强用户体验。
type: docs
weight: 510
url: /zh/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

定义鼠标指针移到形状上时显示的文本。

```csharp
public string ScreenTip { get; set; }
```

## 评论

默认值为空字符串。

## 例子

展示如何插入包含图像且为超链接的形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/”;
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + 左键单击 Microsoft Word 中的形状将打开一个新的 Web 浏览器窗口
// 并将我们带到“HRef”属性中的超链接。
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
