---
title: DocumentBuilder.CurrentSection
linktitle: CurrentSection
articleTitle: CurrentSection
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder CurrentSection 财产. 获取当前在此选择的部分DocumentBuilder 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/documentbuilder/currentsection/
---
## DocumentBuilder.CurrentSection property

获取当前在此选择的部分[`DocumentBuilder`](../).

```csharp
public Section CurrentSection { get; }
```

## 例子

演示如何插入浮动图像，并指定其位置和大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// 配置形状的“RelativeHorizontalPosition”属性以处理“Left”属性的值
// 作为形状距页面左侧的水平距离（以磅为单位）。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// 将形状到页面左侧的水平距离设置为 100。
shape.Left = 100;

// 以类似的方式使用“RelativeVerticalPosition”属性将形状放置在页面顶部下方 80pt 处。
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// 设置形状的高度，这将自动缩放宽度以保留尺寸。
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// “Bottom”和“Right”属性包含图像的下边缘和右边缘。
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### 也可以看看

* class [Section](../../section/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
