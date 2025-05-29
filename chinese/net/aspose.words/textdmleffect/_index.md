---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TextDmlEffect 枚举，使用动态 DML 效果增强文本运行。轻松提升您的文档呈现效果！
type: docs
weight: 7260
url: /zh/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

文本运行的 Dml 文本效果。

```csharp
public enum TextDmlEffect
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Glow | `0` | 发光效果，在对象边缘外添加颜色模糊轮廓。 |
| Fill | `1` | 填充叠加效果。 |
| Shadow | `2` | 阴影效果。 |
| Outline | `3` | 轮廓效果。 |
| Effect3D | `4` | 3D效果. |
| Reflection | `5` | 反射效果。 |

## 例子

展示如何检查运行是否显示 DrawingML 文本效果。

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
