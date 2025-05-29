---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words for .NET
description: 了解如何使用 Aspose.Words 的 Dml3DEffectsRenderingMode 枚举增强您的文档，以实现卓越的 3D 形状渲染和视觉冲击力。
type: docs
weight: 5650
url: /zh/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

指定如何呈现 3D 形状效果。

```csharp
public enum Dml3DEffectsRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Basic | `0` | 基于内部引擎的轻量级稳定渲染， 但使用此模式时不会显示诸如照明、材质和其他附加效果等高级效果。 有关详细信息，请参阅文档。 |
| Advanced | `1` | 渲染扩展的特殊效果列表，包括高级 3D 效果 ，例如斜面、灯光和材质。 |

## 例子

显示如何呈现 3D 效果。

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
