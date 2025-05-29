---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words لـ .NET
description: أمّن مستنداتك مع DocSaveOptions! يمكنك بسهولة تعيين أو استرداد كلمة مرور لتشفير RC4 لحماية معلوماتك الحساسة.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

يحصل على/يحدد كلمة مرور لتشفير المستند باستخدام طريقة تشفير RC4.

```csharp
public string Password { get; set; }
```

## ملاحظات

لحفظ المستند بدون تشفير يجب أن تكون هذه الخاصية`باطل` أو سلسلة فارغة.

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

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
