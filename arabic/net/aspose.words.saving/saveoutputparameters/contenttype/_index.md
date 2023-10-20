---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words لـ .NET
description: SaveOutputParameters ContentType ملكية. إرجاع سلسلة نوع المحتوى نوع وسائط الإنترنت التي تحدد نوع المستند المحفوظ في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

إرجاع سلسلة نوع المحتوى (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ.

```csharp
public string ContentType { get; }
```

## أمثلة

يوضح كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// بعد حفظ المستند، يمكننا الوصول إلى نوع وسائط الإنترنت (نوع MIME) الخاص بمستند الإخراج الذي تم إنشاؤه حديثًا.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// تتغير هذه الخاصية حسب تنسيق الحفظ.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### أنظر أيضا

* class [SaveOutputParameters](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
