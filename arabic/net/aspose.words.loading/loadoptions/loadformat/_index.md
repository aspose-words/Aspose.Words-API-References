---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words لـ .NET
description: LoadOptions LoadFormat ملكية. يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto  في C#.
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

فمن المستحسن أن تحددAuto القيمة والسماح لـ Aspose.Words باكتشاف تنسيق الملف تلقائيًا. إذا كنت تعرف تنسيق المستند الذي أنت على وشك تحميله، فيمكنك تحديد تنسيق بشكل صريح وسيؤدي ذلك إلى تقليل وقت التحميل قليلاً من خلال الحمل المرتبط بالاكتشاف التلقائي للتنسيق. إذا قمت بتحديد تنسيق تحميل صريح وسيتحول إذا تبين أن هذا خطأ، فسيتم استدعاء الاكتشاف التلقائي وسيتم إجراء محاولة ثانية لتحميل الملف.

## أمثلة

يوضح كيفية تحديد عنوان URI أساسي عند فتح مستند html.

```csharp
// لنفترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بمعرف URI نسبي
// أثناء وجود الصورة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل معرف URI النسبي إلى عنوان مطلق.
 // يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// أثناء تعطل الصورة في ملف الإدخال .html، ساعدنا عنوان URI الأساسي المخصص لدينا في إصلاح الرابط.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// سيعرض مستند الإخراج هذا الصورة المفقودة.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### أنظر أيضا

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
