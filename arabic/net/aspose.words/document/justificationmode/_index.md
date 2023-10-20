---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words لـ .NET
description: Document JustificationMode ملكية. الحصول على أو تعيين ضبط تباعد الأحرف في المستند في C#.
type: docs
weight: 230
url: /ar/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

الحصول على أو تعيين ضبط تباعد الأحرف في المستند.

```csharp
public JustificationMode JustificationMode { get; set; }
```

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

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
