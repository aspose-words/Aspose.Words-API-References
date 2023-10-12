---
title: PdfSaveOptions.CacheBackgroundGraphics
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم تخزين الرسومات الموضوعة في خلفية المستند أم لا.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم تخزين الرسومات الموضوعة في خلفية المستند أم لا.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`حقيقي` ويتم كتابة رسومات الخلفية على مستند PDF على هيئة xObject.

عندما تكون القيمة`خطأ شنيع` لا يتم تخزين رسومات الخلفية مؤقتًا.

بعض الأشكال غير مدعومة للتخزين المؤقت (الأشكال التي تحتوي على حقول، وإشارات مرجعية، وHRefs).

رسم خلفية المستند عبارة عن أشكال ومخططات وصور مختلفة يتم وضعها في التذييل أو الرأس، بالإضافة إلى خلفية وحدود الصفحة.

### أمثلة

يوضح كيفية تخزين الرسومات الموضوعة في خلفية المستند مؤقتًا.

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
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


