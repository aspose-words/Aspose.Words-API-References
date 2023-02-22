---
title: DocumentBuilder.MoveToSection
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. ينقل المؤشر إلى بداية النص في قسم محدد.
type: docs
weight: 550
url: /ar/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

ينقل المؤشر إلى بداية النص في قسم محدد.

```csharp
public void MoveToSection(int sectionIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sectionIndex | Int32 | فهرس القسم المراد الانتقال إليه. |

### ملاحظات

عندما يكون sectionIndex أكبر من أو يساوي 0 ، فإنه يحدد فهرس from بداية المستند بحيث يكون 0 هو القسم الأول. عندما يكون sectionIndex أقل من 0 ، فإن يحدد فهرسًا من نهاية المستند بحيث يكون القسم -1 هو القسم الأخير.

يتم نقل المؤشر إلى الفقرة الأولى في ملف **الجسم** من القسم المحدد.

### أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوس وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// أنشئ الرؤوس ، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع رأس.
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

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


