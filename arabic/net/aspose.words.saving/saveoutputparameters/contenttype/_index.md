---
title: SaveOutputParameters.ContentType
second_title: Aspose.Words لمراجع .NET API
description: SaveOutputParameters ملكية. إرجاع سلسلة نوع المحتوى نوع وسائط الإنترنت التي تحدد نوع المستند المحفوظ.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

إرجاع سلسلة نوع المحتوى (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ.

```csharp
public string ContentType { get; }
```

### أمثلة

يوضح كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// بعد أن نحفظ مستندًا ، يمكننا الوصول إلى نوع وسائط الإنترنت (نوع MIME) لمستند الإخراج الذي تم إنشاؤه حديثًا.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// تتغير هذه الخاصية اعتمادًا على تنسيق الحفظ.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### أنظر أيضا

* class [SaveOutputParameters](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoutputparameters/)
* المجسم [Aspose.Words](../../../)


