---
title: DocSaveOptions.Password
second_title: Aspose.Words لمراجع .NET API
description: DocSaveOptions ملكية. الحصول على / تعيين كلمة مرور لتشفير المستند باستخدام طريقة تشفير RC4.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

الحصول على / تعيين كلمة مرور لتشفير المستند باستخدام طريقة تشفير RC4.

```csharp
public string Password { get; set; }
```

### ملاحظات

لحفظ المستند بدون تشفير ، يجب أن تكون هذه الخاصية خالية أو سلسلة فارغة.

### أمثلة

يوضح كيفية تعيين خيارات الحفظ لتنسيقات Microsoft Word القديمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// تعيين كلمة مرور تحمي تحميل المستند بواسطة Microsoft Word أو Aspose.Words.
// لاحظ أن هذا لا يقوم بتشفير محتويات المستند بأي شكل من الأشكال.
options.Password = "MyPassword";

// إذا كان المستند يحتوي على قسيمة توجيه ، فيمكننا الاحتفاظ بها أثناء الحفظ عن طريق ضبط هذه العلامة على "true".
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// لتتمكن من تحميل المستند ،
// سنحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions في كائن LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../docsaveoptions/)
* المجسم [Aspose.Words](../../../)


