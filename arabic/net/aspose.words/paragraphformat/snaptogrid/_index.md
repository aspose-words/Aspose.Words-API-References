---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ParagraphFormat SnapToGrid على تعزيز دقة التخطيط من خلال محاذاة فقراتك مع خطوط شبكة المستند للحصول على مظهر أنيق.
type: docs
weight: 300
url: /ar/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تخطيط المحتويات في الفقرة.

```csharp
public bool SnapToGrid { get; set; }
```

## أمثلة

يوضح كيفية تحديد حد لعدد الأسطر التي يمكن أن تحتوي عليها كل صفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين العرض، ثم استخدمه لتعيين عدد الأسطر في كل صفحة في هذا القسم.
// سيؤدي حجم الخط الكبير بدرجة كافية إلى دفع بعض الأسطر إلى الأسفل إلى الصفحة التالية لتجنب تداخل الأحرف.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
