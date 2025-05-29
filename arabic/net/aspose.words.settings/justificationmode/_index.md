---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words JustificationMode لضبط المسافات بين الأحرف بدقة في مستنداتك. حسّن سهولة القراءة بإعدادات قابلة للتخصيص!
type: docs
weight: 6630
url: /ar/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

يحدد تعديل المسافة بين الأحرف في المستند. القيمة الافتراضية هي`يوسع` .

```csharp
public enum JustificationMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Expand | `0` | لا تضغط المسافة بين الأحرف. |
| Compress | `1` | ضغط المسافة بين الأحرف. |
| CompressKana | `2` | الضغط باستخدام قواعد المقاطع الصوتية الكانا والهيراجانا والكاتاكانا. |

## أمثلة

يوضح كيفية إدارة التحكم في المسافة بين الأحرف.

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
