---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words لـ .NET
description: استكشف مجموعة Aspose.Words.ContentDisposition لاكتشاف خيارات عرض المستندات المختلفة لتحسين تجارب متصفح العميل.
type: docs
weight: 540
url: /ar/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

يقوم بإحصاء الطرق المختلفة لعرض المستند في متصفح العميل.

```csharp
public enum ContentDisposition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Attachment | `0` | إرسال المستند إلى المتصفح وتقديم خيار لحفظ المستند على القرص أو فتحه في التطبيق المرتبط بامتداد المستند. |
| Inline | `1` | إرسال المستند إلى المتصفح ويقدم خيارًا لحفظ المستند على القرص أو فتحه داخل المتصفح. |

## ملاحظات

لاحظ أن السلوك الفعلي على متصفح العميل قد يتأثر بتكوين الأمان الخاص بالمتصفح.

## أمثلة

يوضح كيفية تنفيذ عملية دمج البريد، ثم حفظ المستند في متصفح العميل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

//إرسال المستند إلى متصفح العميل.
//تم إلقاؤه لأن HttpResponse فارغ في الاختبار.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// سوف نحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من عدم إضافة أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.Throws<NullReferenceException>(() => response.End());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
