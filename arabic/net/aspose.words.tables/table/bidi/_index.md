---
title: Table.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: اكتشف خصائص Table Bidi لتنسيق جداول سلس من اليمين إلى اليسار. حسّن تصميم موقعك الإلكتروني بخيارات تخصيص سهلة!
type: docs
weight: 80
url: /ar/net/aspose.words.tables/table/bidi/
---
## Table.Bidi property

يحصل على أو يحدد ما إذا كان هذا جدولًا من اليمين إلى اليسار.

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

متى`حقيقي`، يتم ترتيب الخلايا في هذا الصف من اليمين إلى اليسار.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

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

//قد يؤثر تعيين خصائص نمط الجدول على خصائص الجدول نفسه.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
