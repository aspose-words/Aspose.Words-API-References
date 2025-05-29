---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table LastRow للوصول بسهولة إلى عقدة الصف الأخيرة في جدولك، مما يعزز إدارة البيانات وكفاءتها.
type: docs
weight: 180
url: /ar/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

يعيد آخر[`Row`](../../row/) عقدة في الجدول.

```csharp
public Row LastRow { get; }
```

## أمثلة

يوضح كيفية إزالة الصفوف الأولى والأخيرة من كافة الجداول في مستند.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

### أنظر أيضا

* class [Row](../../row/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
