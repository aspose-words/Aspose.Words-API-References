---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين إدارة المستندات باستخدام خاصية SplitOptions في SplitterContext لتقسيم المحتوى بكفاءة ومرونة. حسّن سير عملك اليوم.
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

خيارات تقسيم المستند.

```csharp
public SplitOptions SplitOptions { get; }
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

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
