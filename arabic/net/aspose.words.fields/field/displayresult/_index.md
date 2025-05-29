---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Field DisplayResult التي توفر النص لنتائج الحقل المعروضة، مما يعزز الوضوح وتجربة المستخدم.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

يحصل على النص الذي يمثل نتيجة الحقل المعروضة.

```csharp
public string DisplayResult { get; }
```

## ملاحظات

ال[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) يجب استدعاء الطريقة للحصول على القيمة الصحيحة لـ [`FieldListNum`](../../fieldlistnum/) ،[`FieldAutoNum`](../../fieldautonum/) ،[`FieldAutoNumOut`](../../fieldautonumout/) و[`FieldAutoNumLgl`](../../fieldautonumlgl/) الحقول.

## أمثلة

يوضح كيفية الحصول على النص الحقيقي الذي يعرضه الحقل في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// يمكننا استخدام خاصية DisplayResult للتحقق من النص الدقيق
//سيتم عرض الحقل في مكانه في المستند.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // لا تحتفظ الحقول بقيم النتائج الدقيقة في الوقت الفعلي.
// للتأكد من أن حقولنا تعرض نتائج دقيقة في أي وقت،
// مثل ما يحدث قبل عملية الحفظ مباشرة، نحتاج إلى تحديثها يدويًا.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
