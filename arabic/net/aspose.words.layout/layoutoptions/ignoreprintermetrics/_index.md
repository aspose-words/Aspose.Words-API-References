---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words لـ .NET
description: LayoutOptions IgnorePrinterMetrics ملكية. الحصول على أو تعيين الإشارة إلى ما إذا كان خيار التوافق استخدام مقاييس الطابعة لتخطيط المستند قد تم تجاهله. الإعداد الافتراضي هوحقيقي  في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

الحصول على أو تعيين الإشارة إلى ما إذا كان خيار التوافق "استخدام مقاييس الطابعة لتخطيط المستند" قد تم تجاهله. الإعداد الافتراضي هو`حقيقي` .

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
