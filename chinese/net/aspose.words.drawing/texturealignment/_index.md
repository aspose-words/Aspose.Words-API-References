---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.TextureAlignment 枚举. 指定纹理填充平铺的对齐方式 在 C#.
type: docs
weight: 1370
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
| TopLeft | `0` | 左上纹理对齐。 |
| Top | `1` | 顶部纹理对齐。 |
| TopRight | `2` | 右上角纹理对齐。 |
| Left | `3` | 左纹理对齐。 |
| Center | `4` | 中心纹理对齐。 |
| Right | `5` | 右纹理对齐。 |
| BottomLeft | `6` | 左下纹理对齐。 |
| Bottom | `7` | 底部纹理对齐。 |
| BottomRight | `8` | 右下纹理对齐。 |
| None | `9` | 无纹理对齐。 |

## 例子

显示如何填充和平铺形状内的纹理。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// 将纹理对齐应用于形状填充。
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// 如果您想获得“TextureAlignment”，请使用合规性选项使用 DML 定义形状
// 文档保存后的属性。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
