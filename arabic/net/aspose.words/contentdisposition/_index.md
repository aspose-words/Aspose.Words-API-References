---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ContentDisposition تعداد. تعداد الطرق المختلفة لعرض المستند في متصفح العميل في C#.
type: docs
weight: 340
url: /ar/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

تعداد الطرق المختلفة لعرض المستند في متصفح العميل.

```csharp
public enum ContentDisposition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Attachment | `0` | أرسل المستند إلى المتصفح وقدم خيارًا لحفظ المستند على القرص أو فتحه في التطبيق المرتبط بامتداد المستند. |
| Inline | `1` | أرسل المستند إلى المتصفح ويقدم خيار حفظ المستند على القرص أو فتحه داخل المتصفح. |

## ملاحظات

لاحظ أن السلوك الفعلي في متصفح العميل قد يتأثر بتكوين أمان المتصفح.

## أمثلة

يوضح كيفية إجراء دمج البريد، ثم حفظ المستند في مستعرض العميل.

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

// أرسل المستند إلى متصفح العميل.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); // تم طرحه لأن HttpResponse فارغ في الاختبار.

// سنحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من أننا لا نضيف أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
