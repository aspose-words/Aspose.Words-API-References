---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words for .NET
description: 设置 TextureAlignment 属性以优化图块纹理填充。轻松自定义对齐方式，增强视觉吸引力和设计精度。
type: docs
weight: 190
url: /zh/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

获取或设置平铺纹理填充的对齐方式。

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## 例子

展示如何填充和平铺形状内的纹理。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// 将纹理对齐应用于形状填充。
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// 如果想要获得“TextureAlignment”，请使用合规性选项通过 DML 定义形状
// 文档保存后的属性。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### 也可以看看

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
