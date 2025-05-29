---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية Table PreferredWidth لتعيين تخطيط الجدول الخاص بك وتحسينه بسهولة لتحسين التصميم وتجربة المستخدم.
type: docs
weight: 220
url: /ar/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

يحصل على العرض المفضل للجدول أو يعينه.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## ملاحظات

القيمة الافتراضية هي[`Auto`](../../preferredwidth/auto/).

## أمثلة

يوضح كيفية ضبط الجدول ليتناسب تلقائيًا مع 50% من عرض الصفحة.

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
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
