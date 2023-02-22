---
title: LayoutOptions.IgnorePrinterMetrics
second_title: Aspose.Words لمراجع .NET API
description: LayoutOptions ملكية. الحصول على أو تعيين إشارة إلى ما إذا كان يتم تجاهل خيار التوافق استخدام مقاييس الطابعة لتخطيط المستند. القيمة الافتراضية هي True .
type: docs
weight: 50
url: /ar/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

الحصول على أو تعيين إشارة إلى ما إذا كان يتم تجاهل خيار التوافق "استخدام مقاييس الطابعة لتخطيط المستند". القيمة الافتراضية هي True .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

### أمثلة

يوضح كيفية تجاهل خيار "استخدام مقاييس الطابعة لتخطيط المستند".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### أنظر أيضا

* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../layoutoptions/)
* المجسم [Aspose.Words](../../../)


