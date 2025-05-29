---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "تنسيق الحفظ" في DocSaveOptions لاختيار تنسيق Doc أو Dot بسهولة لحفظ مستنداتك بسلاسة. حسّن سير عملك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكونDoc أوDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
