---
title: Table.AbsoluteVerticalDistance
linktitle: AbsoluteVerticalDistance
articleTitle: AbsoluteVerticalDistance
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية AbsoluteVerticalDistance للجداول - تحكم في الوضع الرأسي للنقاط للحصول على تخطيط دقيق. القيمة الافتراضية هي 0. حسّن تصميمك!
type: docs
weight: 30
url: /ar/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

يحصل على أو يعين موضع الجدول العائم العمودي المطلق المحدد بواسطة خصائص الجدول، بالنقاط. القيمة الافتراضية هي 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

## أمثلة

يوضح كيفية تعيين موقع الجداول العائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// تعيين موقع الجدول إلى مكان على الصفحة، مثل، في هذه الحالة، الزاوية اليمنى السفلية.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // يمكننا أيضًا تعيين إزاحة أفقية ورأسية بالنقاط من موقع الفقرة التي أدخلنا فيها الجدول.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
