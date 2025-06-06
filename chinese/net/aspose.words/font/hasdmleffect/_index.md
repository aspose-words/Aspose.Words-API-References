---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words for .NET
description: 使用 Font HasDmlEffect 方法检测特定的 DrawingML 文本效果是否已应用。轻松提升文档的视觉吸引力！
type: docs
weight: 570
url: /zh/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

检查是否应用了特定的 DrawingML 文本效果。

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | DrawingML 文本效果类型。 |

### 返回值

`真的`如果应用了特定的 DrawingML 文本效果。

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

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
