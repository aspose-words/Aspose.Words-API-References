---
title: Document.JustificationMode
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على أو تعيين ضبط تباعد الأحرف في المستند.
type: docs
weight: 230
url: /ar/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

الحصول على أو تعيين ضبط تباعد الأحرف في المستند.

```csharp
public JustificationMode JustificationMode { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


