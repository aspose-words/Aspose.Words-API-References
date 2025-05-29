---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.LowCode.SplitterContext لتقسيم المستندات بكفاءة، وتعزيز سير عملك من خلال التكامل السلس والوظائف القوية.
type: docs
weight: 4430
url: /ar/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

سياق تقسيم المستندات.

```csharp
public class SplitterContext : ProcessorContext
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SplitterContext](splittercontext/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | إعدادات الخط المستخدمة بواسطة المعالج. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | خيارات تخطيط المستند التي يستخدمها المعالج. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | خيارات تقسيم المستند. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | استدعاء تحذيري يستخدمه المعالج. |

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

* class [ProcessorContext](../processorcontext/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
