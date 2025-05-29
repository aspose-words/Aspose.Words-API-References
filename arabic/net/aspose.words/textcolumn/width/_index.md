---
title: TextColumn.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية عرض عمود النص لتخصيص عرض عمود النص الخاص بك بسهولة بالنقاط لتحسين التحكم في التخطيط وسهولة القراءة.
type: docs
weight: 20
url: /ar/net/aspose.words/textcolumn/width/
---
## TextColumn.Width property

يحصل على عرض عمود النص بالنقاط أو يعينه.

```csharp
public double Width { get; set; }
```

## أمثلة

يوضح كيفية إنشاء أعمدة متباعدة بشكل غير متساوٍ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// تحديد مقدار المساحة المتوفرة لدينا لترتيب الأعمدة.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// تعيين العمود الأول ليكون ضيقًا.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// قم بتعيين العمود الثاني ليشغل المساحة المتبقية المتوفرة ضمن هوامش الصفحة.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### أنظر أيضا

* class [TextColumn](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
