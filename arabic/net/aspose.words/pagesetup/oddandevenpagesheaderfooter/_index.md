---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words لـ .NET
description: PageSetup OddAndEvenPagesHeaderFooter ملكية. صحيح إذا كان المستند يحتوي على رؤوس وتذييلات مختلفة للصفحات ذات الأرقام الفردية والزوجية في C#.
type: docs
weight: 280
url: /ar/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

صحيح إذا كان المستند يحتوي على رؤوس وتذييلات مختلفة للصفحات ذات الأرقام الفردية والزوجية.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## ملاحظات

لاحظ أن تغيير هذه الخاصية يؤثر على كافة الأقسام في المستند.

## أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// أنشئ الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع رأس.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

يوضح كيفية تمكين أو تعطيل رؤوس/تذييلات الصفحات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يوجد أدناه نوعان من الرؤوس/التذييلات.
// 1 - الرأس/التذييل "الأساسي"، الذي يظهر في كل صفحة في القسم.
 // يمكننا تجاوز الرأس/التذييل الأساسي برأس/تذييل الصفحة الأولى أو الزوجية.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - الرأس/التذييل "الزوجي"، الذي يظهر في كل صفحة زوجية من هذا القسم.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// يحتوي كل قسم على كائن "PageSetup" الذي يحدد الخصائص المتعلقة بمظهر الصفحة
// مثل الاتجاه والحجم والحدود.
// اضبط الخاصية "OddAndEvenPagesHeaderFooter" على "صحيح"
// لعرض رأس/تذييل الصفحة الزوجية على الصفحات الزوجية.
// اضبط الخاصية "OddAndEvenPagesHeaderFooter" على "خطأ"
// لعرض الرأس/التذييل الأساسي على الصفحات الزوجية.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
