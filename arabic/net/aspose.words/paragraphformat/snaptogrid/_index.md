---
title: ParagraphFormat.SnapToGrid
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. يحدد ما إذا كان يجب أن تستخدم الفقرة الحالية خطوط شبكة المستند لكل إعدادات صفحة عند تخطيط المحتويات في الفقرة.
type: docs
weight: 280
url: /ar/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

يحدد ما إذا كان يجب أن تستخدم الفقرة الحالية خطوط شبكة المستند لكل إعدادات صفحة عند تخطيط المحتويات في الفقرة.

```csharp
public bool SnapToGrid { get; set; }
```

### أمثلة

يوضح كيفية تحديد حد لعدد الأسطر التي قد تحتوي عليها كل صفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تمكين الترويج ، ثم استخدمه لتعيين عدد الأسطر لكل صفحة في هذا القسم.
// سيؤدي حجم الخط الكبير بدرجة كافية إلى دفع بعض الأسطر لأسفل في الصفحة التالية لتجنب تداخل الأحرف.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


