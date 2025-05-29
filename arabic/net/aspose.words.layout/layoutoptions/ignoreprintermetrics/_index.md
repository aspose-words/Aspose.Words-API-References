---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LayoutOptions IgnorePrinterMetrics، وتحكم في مقاييس الطابعة لتخطيط المستندات. حسّن التوافق وحسّن دقة الطباعة.
type: docs
weight: 50
url: /ar/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

يحصل على أو يعين مؤشرًا لما إذا كان سيتم تجاهل خيار التوافق "استخدام مقاييس الطابعة لتخطيط المستند". الافتراضي هو`حقيقي` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## أمثلة

يوضح كيفية تجاهل خيار "استخدام مقاييس الطابعة لتخطيط المستند".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### أنظر أيضا

* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
