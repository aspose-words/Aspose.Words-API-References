---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.TextDmlEffect enum لتحسين تشغيل النصوص بتأثيرات DML الديناميكية. ارتقِ بعرض مستندك بسلاسة!
type: docs
weight: 7260
url: /ar/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

تأثير نص Dml لتشغيل النصوص.

```csharp
public enum TextDmlEffect
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Glow | `0` | تأثير التوهج، حيث تتم إضافة مخطط ملون غير واضح خارج حواف الكائن. |
| Fill | `1` | تأثير تراكب التعبئة. |
| Shadow | `2` | تأثير الظل. |
| Outline | `3` | تأثير المخطط التفصيلي. |
| Effect3D | `4` | تأثير ثلاثي الأبعاد. |
| Reflection | `5` | تأثير الانعكاس. |

## أمثلة

يوضح كيفية التحقق مما إذا كان التشغيل يعرض تأثير نص DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
