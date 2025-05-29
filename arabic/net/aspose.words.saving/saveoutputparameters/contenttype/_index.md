---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveOutputParameters ContentType، التي توفر نوع الوسائط على الإنترنت للمستندات المحفوظة لديك، مما يضمن التعرف الدقيق على الملف.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

يعيد سلسلة نوع المحتوى (نوع الوسائط عبر الإنترنت) التي تحدد نوع المستند المحفوظ.

```csharp
public string ContentType { get; }
```

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

* class [SaveOutputParameters](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
