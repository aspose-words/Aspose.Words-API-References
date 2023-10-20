---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words لـ .NET
description: DocSaveOptions Password ملكية. الحصول على/تعيين كلمة مرور لتشفير المستند باستخدام طريقة التشفير RC4 في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

الحصول على/تعيين كلمة مرور لتشفير المستند باستخدام طريقة التشفير RC4.

```csharp
public string Password { get; set; }
```

## ملاحظات

من أجل حفظ المستند بدون تشفير، يجب أن تكون هذه الخاصية`باطل` أو سلسلة فارغة.

## أمثلة

يوضح كيفية تعيين خيارات الحفظ لتنسيقات Microsoft Word الأقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// قم بتعيين كلمة مرور تحمي تحميل المستند بواسطة Microsoft Word أو Aspose.Words.
// لاحظ أن هذا لا يؤدي إلى تشفير محتويات المستند بأي شكل من الأشكال.
options.Password = "MyPassword";

// إذا كانت الوثيقة تحتوي على قسيمة توجيه، فيمكننا الحفاظ عليها أثناء الحفظ عن طريق تعيين هذه العلامة على "صحيح".
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// لتتمكن من تحميل المستند،
// سنحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions في كائن LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
