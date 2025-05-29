---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.TextureAlignment 枚举，实现精确的纹理填充对齐。使用无缝平铺选项增强您的文档设计！
type: docs
weight: 1780
url: /zh/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

指定纹理填充平铺的对齐方式。

```csharp
public enum TextureAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| TopLeft | `0` | 左上角纹理对齐。 |
| Top | `1` | 顶部纹理对齐。 |
| TopRight | `2` | 右上角纹理对齐。 |
| Left | `3` | 左纹理对齐。 |
| Center | `4` | 中心纹理对齐。 |
| Right | `5` | 右纹理对齐。 |
| BottomLeft | `6` | 左下角纹理对齐。 |
| Bottom | `7` | 底部纹理对齐。 |
| BottomRight | `8` | 右下角纹理对齐。 |
| None | `9` | 无纹理对齐。 |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
