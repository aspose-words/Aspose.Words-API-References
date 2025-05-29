---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfSaveOptions CacheBackgroundGraphics لتحسين تخزين رسومات المستندات مؤقتًا، مما يعزز إنشاء ملفات PDF وأدائها.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

يحصل على قيمة تحدد ما إذا كان سيتم تخزين الرسومات الموضوعة في خلفية المستند أم لا.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` ويتم كتابة الرسومات الخلفية في مستند PDF كـ xObject.

عندما تكون القيمة`خطأ شنيع` لا يتم تخزين الرسومات الخلفية مؤقتًا.

بعض الأشكال غير مدعومة للتخزين المؤقت (الأشكال التي تحتوي على حقول وإشارات مرجعية وHRefs).

تتكون خلفية المستند من أشكال مختلفة ومخططات وصور توضع في التذييل أو الرأس، بالإضافة إلى الخلفية وحدود الصفحة.

## أمثلة

يوضح كيفية تخزين الرسومات الموجودة في خلفية المستند.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
