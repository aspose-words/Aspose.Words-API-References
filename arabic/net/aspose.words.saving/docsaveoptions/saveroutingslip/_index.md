---
title: DocSaveOptions.SaveRoutingSlip
linktitle: SaveRoutingSlip
articleTitle: SaveRoutingSlip
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية حفظ توجيه مستندات DocSaveOptions. تحكّم في حفظ بيانات توجيه مستنداتك. حسّن تخصيص الإخراج بسهولة!
type: docs
weight: 70
url: /ar/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

عندما`خطأ شنيع` لا يتم حفظ بيانات RoutingSlip في مستند الإخراج. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool SaveRoutingSlip { get; set; }
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

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
