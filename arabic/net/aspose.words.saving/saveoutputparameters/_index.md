---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.SaveOutputParameters، التي توفر تفاصيل أساسية بعد حفظ المستند، مما يعزز تجربة إدارة المستندات لديك.
type: docs
weight: 6390
url: /ar/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

يُعاد هذا الكائن إلى المُستدعي بعد حفظ المستند، ويحتوي على معلومات إضافية تُفيد بأن قد تم إنشاؤه أو حسابه أثناء عملية الحفظ. يُمكن للمُستدعي استخدام هذا الكائن أو تجاهله.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class SaveOutputParameters
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | يعيد سلسلة نوع المحتوى (نوع الوسائط عبر الإنترنت) التي تحدد نوع المستند المحفوظ. |

## أمثلة

يوضح كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// بعد حفظ المستند، يمكننا الوصول إلى نوع الوسائط على الإنترنت (نوع MIME) للمستند الناتج الذي تم إنشاؤه حديثًا.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// تتغير هذه الخاصية وفقًا لتنسيق الحفظ.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
