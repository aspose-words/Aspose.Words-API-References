---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين تباعد الأحرف في مستندك باستخدام خاصية JustificationMode. حسّن سهولة القراءة وحسّن العرض بسهولة!
type: docs
weight: 240
url: /ar/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

يحصل على تعديل المسافة بين أحرف المستند أو يعينه.

```csharp
public JustificationMode JustificationMode { get; set; }
```

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

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
