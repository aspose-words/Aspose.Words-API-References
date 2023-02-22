---
title: TextColumn.SpaceAfter
second_title: Aspose.Words لمراجع .NET API
description: TextColumn ملكية. الحصول على أو تحديد المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير.
type: docs
weight: 10
url: /ar/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

الحصول على أو تحديد المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير.

```csharp
public double SpaceAfter { get; set; }
```

### أمثلة

يوضح كيفية إنشاء أعمدة متباعدة بشكل غير متساو.

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

// اضبط العمود الثاني ليأخذ باقي المساحة المتوفرة ضمن هوامش الصفحة.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### أنظر أيضا

* class [TextColumn](../)
* مساحة الاسم [Aspose.Words](../../textcolumn/)
* المجسم [Aspose.Words](../../../)


