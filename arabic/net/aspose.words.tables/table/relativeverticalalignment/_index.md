---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table RelativeVerticalAlignment لإدارة المحاذاة الرأسية بسهولة للجداول العائمة، مما يعزز دقة تخطيطك وتصميمه.
type: docs
weight: 240
url: /ar/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

يحصل على محاذاة الجدول العائم الرأسية النسبية أو يعينها.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
