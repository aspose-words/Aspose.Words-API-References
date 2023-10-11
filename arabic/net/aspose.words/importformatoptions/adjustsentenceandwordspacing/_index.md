---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
second_title: Aspose.Words لمراجع .NET API
description: ImportFormatOptions ملكية. الحصول على قيمة منطقية أو تعيينها والتي تحدد ما إذا كان سيتم ضبط تباعد الجملة والكلمات تلقائيًا. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 20
url: /ar/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

الحصول على قيمة منطقية أو تعيينها والتي تحدد ما إذا كان سيتم ضبط تباعد الجملة والكلمات تلقائيًا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

### أمثلة

يوضح كيفية ضبط تباعد الجملة والكلمات تلقائيًا.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../importformatoptions/)
* المجسم [Aspose.Words](../../../)


