---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextColumn SpaceAfter لضبط المسافات بين الأعمدة في تخطيطك بسهولة. حسّن سهولة القراءة والتصميم بدقة!
type: docs
weight: 10
url: /ar/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

يُحدِّد المسافة بين هذا العمود والعمود التالي بالنقاط، أو يُحدِّدها. غير مطلوب للعمود الأخير.

```csharp
public double SpaceAfter { get; set; }
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
