---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إنشاء مثيل جديد لمعالج التقسيم بكفاءة باستخدام دليلنا السهل المتابعة لتحقيق التكامل السلس والأداء المحسن.
type: docs
weight: 10
url: /ar/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

ينشئ مثيلًا جديدًا لمعالج التقسيم.

```csharp
public static Splitter Create(SplitterContext context)
```

## أمثلة

يوضح كيفية تقسيم المستند حسب الصفحات باستخدام السياق.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

يوضح كيفية تقسيم المستند من التدفق حسب الصفحات باستخدام السياق.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### أنظر أيضا

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
