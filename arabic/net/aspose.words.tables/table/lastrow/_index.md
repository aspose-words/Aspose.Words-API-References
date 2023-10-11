---
title: Table.LastRow
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. إرجاع الأخيرRow العقدة في الجدول.
type: docs
weight: 180
url: /ar/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

إرجاع الأخير[`Row`](../../row/) العقدة في الجدول.

```csharp
public Row LastRow { get; }
```

### أمثلة

يوضح كيفية إزالة الصفين الأول والأخير من كافة الجداول في المستند.

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
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


