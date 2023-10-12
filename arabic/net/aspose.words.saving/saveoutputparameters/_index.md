---
title: Class SaveOutputParameters
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.SaveOutputParameters فصل. يتم إرجاع هذا الكائن إلى المتصل بعد حفظ المستند ويحتوي على معلومات إضافية تم إنشاؤها أو حسابها بواسطة أثناء عملية الحفظ. يمكن للمتصل استخدام هذا الكائن أو تجاهله.
type: docs
weight: 5590
url: /ar/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

يتم إرجاع هذا الكائن إلى المتصل بعد حفظ المستند ويحتوي على معلومات إضافية تم إنشاؤها أو حسابها بواسطة أثناء عملية الحفظ. يمكن للمتصل استخدام هذا الكائن أو تجاهله.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class SaveOutputParameters
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | إرجاع سلسلة نوع المحتوى (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ. |

### أمثلة

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


