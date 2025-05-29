---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.IncorrectPasswordException، التي تتعامل مع أخطاء كلمة المرور للمستندات المشفرة، مما يضمن وصولاً آمنًا وسلسًا.
type: docs
weight: 3700
url: /ar/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

يتم طرحه إذا تم تشفير مستند بكلمة مرور وكانت كلمة المرور المحددة عند فتح المستند غير صحيحة أو مفقودة.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class IncorrectPasswordException : Exception
```

## أمثلة

يوضح كيفية تعيين خيارات الحفظ لتنسيقات Microsoft Word القديمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// تعيين كلمة مرور لحماية تحميل المستند بواسطة Microsoft Word أو Aspose.Words.
// لاحظ أن هذا لا يقوم بتشفير محتويات المستند بأي شكل من الأشكال.
options.Password = "MyPassword";

// إذا كانت الوثيقة تحتوي على إشعار توجيه، فيمكننا الحفاظ عليها أثناء الحفظ عن طريق تعيين هذا العلم على true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// لكي تتمكن من تحميل المستند،
// سوف نحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions في كائن LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
