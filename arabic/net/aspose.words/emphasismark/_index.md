---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words لـ .NET
description: Aspose.Words.EmphasisMark تعداد. يحدد الأنواع المحتملة لعلامات التركيز في C#.
type: docs
weight: 1460
url: /ar/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

يحدد الأنواع المحتملة لعلامات التركيز.

```csharp
public enum EmphasisMark
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا توجد علامة تأكيد. |
| OverSolidCircle | `1` | علامة التوكيد عبارة عن دائرة سوداء صلبة معروضة أعلى النص. |
| OverComma | `2` | علامة التوكيد هي حرف فاصلة يتم عرضه فوق النص. |
| OverWhiteCircle | `3` | علامة التوكيد عبارة عن دائرة بيضاء فارغة معروضة أعلى النص. |
| UnderSolidCircle | `4` | علامة التوكيد عبارة عن دائرة سوداء صلبة معروضة أسفل النص. |

## أمثلة

يوضح كيفية إضافة حرف إضافي معروض أعلى/أسفل الحرف الرسومي.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// الأنواع المحتملة لعلامة التركيز:
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
