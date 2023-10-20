---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Settings.JustificationMode تعداد. يحدد تعديل تباعد الأحرف للمستند. القيمة الافتراضية هييوسع  في C#.
type: docs
weight: 5800
url: /ar/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

يحدد تعديل تباعد الأحرف للمستند. القيمة الافتراضية هي`يوسع` .

```csharp
public enum JustificationMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

## أمثلة

يوضح كيفية إدارة التحكم في تباعد الأحرف.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)                
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
