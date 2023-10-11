---
title: Table.PreferredWidth
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على العرض المفضل للجدول أو تعيينه.
type: docs
weight: 220
url: /ar/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

الحصول على العرض المفضل للجدول أو تعيينه.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

### ملاحظات

القيمة الافتراضية هي[`Auto`](../../preferredwidth/auto/).

### أمثلة

يوضح كيفية تعيين جدول ليتناسب تلقائيًا مع 50% من عرض الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### أنظر أيضا

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


