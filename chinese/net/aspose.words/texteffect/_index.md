---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TextEffect 枚举，实现动态文本动画。使用引人入胜的效果增强您的文档，打造引人入胜的用户体验。
type: docs
weight: 7270
url: /zh/net/aspose.words/texteffect/
---
## TextEffect enumeration

文本运行的动画效果。

```csharp
public enum TextEffect
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## 例子

展示如何将视觉效果应用于运行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// 旧版本的 Microsoft Word 仅支持字体动画效果。
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
