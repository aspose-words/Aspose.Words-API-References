---
title: ParagraphFormat.WidowControl
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. صحيح إذا كان السطر الأول والأخير في الفقرة سيظلان في نفس الصفحة كبقية الفقرة .
type: docs
weight: 390
url: /ar/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

صحيح إذا كان السطر الأول والأخير في الفقرة سيظلان في نفس الصفحة كبقية الفقرة .

```csharp
public bool WidowControl { get; set; }
```

### أمثلة

يوضح كيفية تمكين عنصر التحكم بالأسطر الناقصة / الوحيدة للفقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// عندما نكتب النص الذي لا يتناسب مع صفحة واحدة ، فقد يمتد سطر واحد إلى الصفحة التالية.
// السطر الفردي الذي ينتهي في الصفحة التالية يسمى "اليتيم" ،
// والسطر السابق الذي انقطع فيه اليتيم يسمى "الأرملة".
// يمكننا إصلاح الأيتام والأرامل عن طريق إعادة ترتيب النص عبر حجم الخط أو التباعد أو هوامش الصفحة.
// إذا كنا نرغب في الحفاظ على أبعاد وثيقتنا ، فيمكننا ضبط هذه العلامة على "true"
 // لدفع الأرامل إلى نفس الصفحة مع أيتامهم.
// اترك هذه العلامة على أنها "خطأ" ستترك أزواج الأرملة / اليتيم في النص.
// تحتوي كل فقرة على هذا الإعداد الذي يمكن الوصول إليه في Microsoft Word عبر الصفحة الرئيسية - >; فقرة - >. إعدادات الفقرة
// (الزر الموجود في الركن الأيمن السفلي من علامة التبويب "الفقرة") - >; "التحكم بالأسطر الناقصة / اليتيم".
builder.ParagraphFormat.WidowControl = widowControl; 

// أدخل النص الذي ينتج عنه يتيم وأرملة.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


