---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words لـ .NET
description: ParagraphFormat SnapToGrid ملكية. يحدد ما إذا كان يجب على الفقرة الحالية استخدام خطوط شبكة المستند لكل صفحة settings عند تخطيط المحتويات في الفقرة في C#.
type: docs
weight: 290
url: /ar/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

يحدد ما إذا كان يجب على الفقرة الحالية استخدام خطوط شبكة المستند لكل صفحة settings عند تخطيط المحتويات في الفقرة.

```csharp
public bool SnapToGrid { get; set; }
```

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

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
