---
title: TableStyle.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words لـ .NET
description: TableStyle Alignment ملكية. يحدد المحاذاة لنمط الجدول في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/tablestyle/alignment/
---
## TableStyle.Alignment property

يحدد المحاذاة لنمط الجدول.

```csharp
public TableAlignment Alignment { get; set; }
```

## ملاحظات

القيمة الافتراضية هيLeft .

## أمثلة

يوضح كيفية ضبط موضع الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لمحاذاة الجدول أفقيًا.
// 1 - استخدم خاصية "المحاذاة" لمحاذاتها لموقع في الصفحة، مثل المركز:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// أدخل جدولاً وقم بتطبيق النمط الذي أنشأناه عليه.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - استخدم "LeftIndent" لتحديد مسافة بادئة من الهامش الأيسر للصفحة:
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### أنظر أيضا

* enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* class [TableStyle](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
