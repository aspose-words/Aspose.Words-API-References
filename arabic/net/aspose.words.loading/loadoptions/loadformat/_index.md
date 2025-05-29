---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LoadOptions LoadFormat لتحديد تنسيقات المستندات بسهولة. حسّن التحميل باستخدام الإعداد التلقائي الافتراضي لأداء سلس.
type: docs
weight: 90
url: /ar/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## ملاحظات

من المستحسن أن تحددAuto القيمة، ودع Aspose.Words يكتشف تنسيق الملف تلقائيًا. إذا كنت تعرف تنسيق المستند الذي ستحمّله، يمكنك تحديد format صراحةً، مما سيقلل من وقت التحميل بشكل طفيف بسبب التكلفة الإضافية المرتبطة بالكشف التلقائي عن format . إذا حددت تنسيق تحميل صريحًا وتبين أنه خاطئ، فسيتم تفعيل الكشف التلقائي وستُجرى محاولة ثانية لتحميل الملف.

## أمثلة

يوضح كيفية تحديد عنوان URI الأساسي عند فتح مستند html.

```csharp
// افترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بمعرف URI نسبي
// بينما الصورة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل عنوان URI النسبي إلى عنوان URI مطلق.
 // يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// بينما كانت الصورة معطلة في ملف .html المدخل، ساعدنا عنوان URI الأساسي المخصص في إصلاح الرابط.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// ستعرض وثيقة الإخراج هذه الصورة المفقودة.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### أنظر أيضا

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
