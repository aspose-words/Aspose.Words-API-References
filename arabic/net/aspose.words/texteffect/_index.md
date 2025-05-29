---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words لـ .NET
description: استكشف مجموعة Aspose.Words.TextEffect لرسومات نصية ديناميكية. حسّن مستنداتك بتأثيرات جذابة لتجربة مستخدم آسرة.
type: docs
weight: 7270
url: /ar/net/aspose.words/texteffect/
---
## TextEffect enumeration

تأثير الرسوم المتحركة لتشغيل النص.

```csharp
public enum TextEffect
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## أمثلة

يوضح كيفية تطبيق تأثير مرئي على الجري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// تدعم الإصدارات الأقدم من Microsoft Word تأثيرات الرسوم المتحركة للخطوط فقط.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
