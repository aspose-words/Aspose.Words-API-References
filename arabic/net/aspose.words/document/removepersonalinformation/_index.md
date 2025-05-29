---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words لـ .NET
description: تأكد من الخصوصية باستخدام ميزة إزالة المعلومات الشخصية للمستند في Word، والتي تقوم تلقائيًا بحذف بيانات المستخدم من التعليقات والخصائص عند الحفظ.
type: docs
weight: 360
url: /ar/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

يحصل على أو يعين علمًا يشير إلى أن Microsoft Word سيقوم بإزالة جميع معلومات المستخدم من التعليقات والمراجعات وخصائص المستند عند حفظ المستند.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## أمثلة

يوضح كيفية تمكين إزالة المعلومات الشخصية أثناء الحفظ اليدوي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدخل بعض المحتوى الذي يحتوي على معلومات شخصية.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// هذا العلم يعادل ملف -> خيارات -> مركز التوثيق -> إعدادات مركز التوثيق... ->
// خيارات الخصوصية -> "إزالة المعلومات الشخصية من خصائص الملف عند الحفظ" في Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// لن يتم تطبيق هذا الخيار أثناء عملية الحفظ التي يتم إجراؤها باستخدام Aspose.Words.
// سيتم إزالة البيانات الشخصية من مستندنا مع تعيين العلم عندما نحفظه يدويًا باستخدام Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
