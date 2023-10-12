---
title: TableStyle.CellSpacing
second_title: Aspose.Words لمراجع .NET API
description: TableStyle ملكية. الحصول على أو تعيين مقدار المسافة بالنقاط بين الخلايا.
type: docs
weight: 60
url: /ar/net/aspose.words/tablestyle/cellspacing/
---
## TableStyle.CellSpacing property

الحصول على أو تعيين مقدار المسافة (بالنقاط) بين الخلايا.

```csharp
public double CellSpacing { get; set; }
```

### أمثلة

يوضح كيفية إنشاء إعدادات نمط مخصصة للجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// قد يؤثر تعيين خصائص نمط الجدول على خصائص الجدول نفسه.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### أنظر أيضا

* class [TableStyle](../)
* مساحة الاسم [Aspose.Words](../../tablestyle/)
* المجسم [Aspose.Words](../../../)


