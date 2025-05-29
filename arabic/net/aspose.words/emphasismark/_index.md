---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.EmphasisMark enum، الذي يضم أنواعًا متنوعة من التوكيد لتحسين تنسيق مستندك. عزز تأثير نصك اليوم!
type: docs
weight: 1870
url: /ar/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

يحدد أنواع علامات التأكيد الممكنة.

```csharp
public enum EmphasisMark
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يوجد علامة توكيد. |
| OverSolidCircle | `1` | علامة التأكيد هي عبارة عن دائرة سوداء متصلة تظهر أعلى النص. |
| OverComma | `2` | علامة التأكيد هي حرف فاصلة يظهر أعلى النص. |
| OverWhiteCircle | `3` | علامة التأكيد هي عبارة عن دائرة بيضاء فارغة تظهر أعلى النص. |
| UnderSolidCircle | `4` | علامة التأكيد هي عبارة عن دائرة سوداء متصلة تظهر أسفل النص. |

## أمثلة

يوضح كيفية إضافة حرف إضافي يتم عرضه أعلى/أسفل الحرف الرسومي.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// أنواع علامات التأكيد المحتملة:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
