---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية SplitOptions SplitCriteria على تعزيز إدارة المستندات من خلال تقسيم المحتوى الخاص بك بكفاءة إلى أقسام قابلة للإدارة.
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

يحدد معايير تقسيم المستند إلى أجزاء.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## أمثلة

يوضح كيفية تقسيم المستند حسب الصفحات.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### أنظر أيضا

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
