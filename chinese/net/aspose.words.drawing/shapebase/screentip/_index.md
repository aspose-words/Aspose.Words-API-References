---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase ScreenTip 财产. 定义当鼠标指针移到形状上时显示的文本 在 C#.
type: docs
weight: 480
url: /zh/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

定义当鼠标指针移到形状上时显示的文本。

```csharp
public string ScreenTip { get; set; }
```

## 评论

默认值为空字符串。

## 例子

显示如何插入包含图像的形状，也是超链接。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
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
