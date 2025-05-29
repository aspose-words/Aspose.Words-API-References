---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
articleTitle: AdjustSentenceAndWordSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImportFormatOptions AdjustSentenceAndWordSpacing. تحكم بسهولة في المسافات التلقائية بين الجمل والكلمات لتحسين وضوح النص.
type: docs
weight: 20
url: /ar/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

يحصل على قيمة منطقية أو يعينها لتحديد ما إذا كان سيتم تعديل المسافة بين الجمل والكلمات تلقائيًا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## أمثلة

يوضح كيفية ضبط المسافة بين الجمل والكلمات تلقائيًا.

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
