---
title: Table.AbsoluteHorizontalDistance
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على أو تعيين موضع الجدول العائم الأفقي المطلق المحدد بواسطة خصائص الجدول بالنقاط. القيمة الافتراضية هي 0.
type: docs
weight: 20
url: /ar/net/aspose.words.tables/table/absolutehorizontaldistance/
---
## Table.AbsoluteHorizontalDistance property

الحصول على أو تعيين موضع الجدول العائم الأفقي المطلق المحدد بواسطة خصائص الجدول، بالنقاط. القيمة الافتراضية هي 0.

```csharp
public double AbsoluteHorizontalDistance { get; set; }
```

### أمثلة

يوضح كيفية ضبط موقع الجداول العائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// قم بتعيين موقع الجدول في مكان على الصفحة، مثل، في هذه الحالة، الزاوية اليمنى السفلية.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // يمكننا أيضًا تعيين إزاحة أفقية ورأسية في النقاط من موقع الفقرة حيث قمنا بإدراج الجدول.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


