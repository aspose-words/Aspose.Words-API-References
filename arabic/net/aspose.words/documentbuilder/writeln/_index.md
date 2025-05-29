---
title: DocumentBuilder.Writeln
linktitle: Writeln
articleTitle: Writeln
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة Writeln في DocumentBuilder—أدخل النصوص وفواصل الفقرات بسلاسة لتحسين قابلية القراءة.
type: docs
weight: 700
url: /ar/net/aspose.words/documentbuilder/writeln/
---
## Writeln(*string*) {#writeln_1}

يقوم بإدراج سلسلة وفاصل فقرة في المستند.

```csharp
public void Writeln(string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | السلسلة التي سيتم إدراجها في المستند. |

## ملاحظات

الخط الحالي وتنسيق الفقرة المحدد بواسطة[`Font`](../font/) و[`ParagraphFormat`](../paragraphformat/) يتم استخدام الخصائص.

## أمثلة

يوضح كيفية إنشاء جدول 2x2 منسق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// أثناء إنشاء الجدول، سيقوم منشئ المستند بتطبيق قيم خصائص RowFormat/CellFormat الحالية
// إلى الصف/الخلية الحالية التي يتواجد بها المؤشر وأي صفوف/خلايا جديدة أثناء إنشائها.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// لا تتأثر الصفوف والخلايا المضافة مسبقًا بأثر رجعي بالتغييرات التي تطرأ على تنسيق المنشئ.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Writeln() {#writeln}

يقوم بإدراج فاصل فقرة في المستند.

```csharp
public void Writeln()
```

## ملاحظات

المكالمات[`InsertParagraph`](../insertparagraph/).

## أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// قم بإنشاء الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من أنواع الرؤوس.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
