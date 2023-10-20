---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words لـ .NET
description: PageSetup LinesPerPage ملكية. الحصول على أو تعيين عدد الأسطر لكل صفحة في شبكة المستند في C#.
type: docs
weight: 240
url: /ar/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

الحصول على أو تعيين عدد الأسطر لكل صفحة في شبكة المستند.

```csharp
public int LinesPerPage { get; set; }
```

## ملاحظات

الحد الأدنى لقيمة الخاصية هو 1. وتعتمد القيمة القصوى على ارتفاع الصفحة وحجم الخط للنمط Normal . الحد الأدنى لمسافة الخط هو 136 بالمائة من حجم الخط. على سبيل المثال، الحد الأقصى لعدد الأسطر في كل صفحة صفحة Letter بهامش بوصة واحدة هو 39.

بشكل افتراضي، تحتوي الخاصية على قيمة، حيث تكون خطوة الخط أكبر بمقدار 1.5 مرة من حجم الخط بالنمط العادي.

## أمثلة

يوضح كيفية تحديد حد لعدد الأسطر التي قد تحتوي عليها كل صفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين العرض، ثم استخدمه لتعيين عدد الأسطر لكل صفحة في هذا القسم.
// سيؤدي حجم الخط الكبير بدرجة كافية إلى دفع بعض الأسطر لأسفل إلى الصفحة التالية لتجنب تداخل الأحرف.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
