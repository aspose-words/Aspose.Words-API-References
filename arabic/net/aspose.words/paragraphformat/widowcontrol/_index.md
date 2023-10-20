---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words لـ .NET
description: ParagraphFormat WidowControl ملكية. صحيح إذا كان السطر الأول والأخير في الفقرة سيبقى في نفس الصفحة مثل بقية الفقرة في C#.
type: docs
weight: 400
url: /ar/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

صحيح إذا كان السطر الأول والأخير في الفقرة سيبقى في نفس الصفحة مثل بقية الفقرة.

```csharp
public bool WidowControl { get; set; }
```

## أمثلة

يوضح كيفية تمكين التحكم في الأرملة/اليتيم لفقرة ما.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// عندما نكتب نصًا لا يتناسب مع صفحة واحدة، فقد يمتد سطر واحد إلى الصفحة التالية.
// السطر الوحيد الذي ينتهي في الصفحة التالية يسمى "اليتيم"،
// والسطر السابق الذي انقطع فيه اليتيم يسمى "أرملة".
// يمكننا إصلاح الأيتام والأرامل عن طريق إعادة ترتيب النص حسب حجم الخط أو التباعد أو هوامش الصفحة.
// إذا أردنا الحفاظ على أبعاد وثيقتنا، يمكننا ضبط هذه العلامة على "صحيح"
 // لدفع الأرامل إلى نفس الصفحة مثل أيتامهن.
// ترك هذه العلامة كـ "خطأ" سيؤدي إلى ترك أزواج الأرملة/الأيتام في النص.
// يمكن الوصول إلى هذا الإعداد في كل فقرة في Microsoft Word عبر الصفحة الرئيسية -> فقرة -> إعدادات الفقرة
// (الزر الموجود أسفل الجانب الأيمن من علامة التبويب "فقرة") -> “السيطرة على الأرملة / اليتيم”.
builder.ParagraphFormat.WidowControl = widowControl; 

// أدخل نصًا ينتج عنه يتيمًا وأرملة.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
