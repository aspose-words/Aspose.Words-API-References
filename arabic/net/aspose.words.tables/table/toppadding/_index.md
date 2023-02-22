---
title: Table.TopPadding
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على أو تحديد مقدار المساحة بالنقاط للإضافة فوق محتويات الخلايا.
type: docs
weight: 330
url: /ar/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

الحصول على أو تحديد مقدار المساحة (بالنقاط) للإضافة فوق محتويات الخلايا.

```csharp
public double TopPadding { get; set; }
```

### أمثلة

يوضح كيفية تكوين المحتوى المتراكم في جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

// لكل خلية في الجدول ، عيّن المسافة بين محتوياتها وكل من حدودها. 
// سيحافظ هذا الجدول على الحد الأدنى لمسافة المساحة المتروكة عن طريق التفاف النص.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


