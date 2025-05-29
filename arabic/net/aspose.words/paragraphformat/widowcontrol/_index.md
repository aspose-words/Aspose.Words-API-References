---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تضمن خاصية ParagraphFormat WidowControl بقاء الأسطر الأولى والأخيرة من النص معًا على نفس الصفحة لتحسين قابلية القراءة.
type: docs
weight: 410
url: /ar/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

صحيح إذا كان من المقرر أن يظل السطر الأول والأخير في الفقرة على نفس الصفحة مثل بقية الفقرة.

```csharp
public bool WidowControl { get; set; }
```

## أمثلة

يوضح كيفية تمكين التحكم بالأرملة/اليتيم للفقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// عندما نكتب نصًا لا يتناسب مع صفحة واحدة، فقد يمتد سطر واحد إلى الصفحة التالية.
// السطر الوحيد الذي ينتهي في الصفحة التالية يسمى "يتيم"،
// والسطر السابق حيث انقطع اليتيم يسمى "أرملة".
// يمكننا إصلاح الأيتام والأرامل عن طريق إعادة ترتيب النص من خلال حجم الخط أو التباعد أو هوامش الصفحة.
// إذا أردنا الحفاظ على أبعاد مستندنا، فيمكننا تعيين هذا العلم على "صحيح"
// لدفع الأرامل إلى نفس الصفحة مع أيتامهم.
// ترك هذا العلم على "خطأ" سيؤدي إلى ترك أزواج الأرامل/الأيتام في النص.
// كل فقرة لديها هذا الإعداد الذي يمكن الوصول إليه في Microsoft Word عبر الصفحة الرئيسية -> الفقرة -> إعدادات الفقرة
// (الزر الموجود في الزاوية اليمنى السفلية من علامة التبويب "فقرة") -> "التحكم في الأرامل/اليتامى".
builder.ParagraphFormat.WidowControl = widowControl; 

//إدراج نص ينتج يتيمًا وأرملة.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
