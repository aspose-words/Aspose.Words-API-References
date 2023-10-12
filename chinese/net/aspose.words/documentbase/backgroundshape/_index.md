---
title: DocumentBase.BackgroundShape
second_title: Aspose.Words for .NET API 参考
description: DocumentBase 财产. 获取或设置文档的背景形状可无效的.
type: docs
weight: 10
url: /zh/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

获取或设置文档的背景形状。可`无效的`.

```csharp
public Shape BackgroundShape { get; set; }
```

### 评论

Microsoft Word 只允许具有其自身形状的形状[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/)属性 equal 至Rectangle用作文档的背景形状。

Microsoft Word 仅支持背景形状的填充属性。所有其他属性 都将被忽略。

将此属性设置为非空值也会设置[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/)到`真的`。

### 例子

演示如何为文档的每个页面设置背景形状。

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// 我们可以用作背景的唯一形状类型是矩形。
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// 有两种方法可以使用此形状作为页面背景。
// 1 - 平面颜色：
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - 图像：
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// 调整图像的外观，使其更适合作为水印。
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word 不支持以图像为背景的形状，
// 但我们仍然可以以其他保存格式（例如 .pdf）看到这些背景。
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../documentbase/)
* 部件 [Aspose.Words](../../../)


