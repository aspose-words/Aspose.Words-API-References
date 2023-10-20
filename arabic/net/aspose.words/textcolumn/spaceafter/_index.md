---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words لـ .NET
description: TextColumn SpaceAfter ملكية. الحصول على أو تعيين المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

الحصول على أو تعيين المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير.

```csharp
public double SpaceAfter { get; set; }
```

## أمثلة

يوضح كيفية إنشاء أعمدة متباعدة بشكل غير متساو.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// حدد مقدار المساحة المتوفرة لدينا لترتيب الأعمدة.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// قم بتعيين العمود الأول ليكون ضيقًا.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// اضبط العمود الثاني ليأخذ باقي المساحة المتوفرة في هوامش الصفحة.
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
