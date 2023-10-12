---
title: Table.FirstRow
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. إرجاع الأولRow العقدة في الجدول.
type: docs
weight: 160
url: /ar/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

إرجاع الأول[`Row`](../../row/) العقدة في الجدول.

```csharp
public Row FirstRow { get; }
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

يوضح كيفية دمج الصفوف من جدولين في جدول واحد.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// فيما يلي طريقتان للحصول على جدول من مستند.
// 1 - من مجموعة "الجداول" للعقدة الأساسية:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - استخدام طريقة "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// إلحاق جميع الصفوف من الجدول الحالي بالجدول التالي.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// قم بإزالة حاوية الجدول الفارغة.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### أنظر أيضا

* class [Row](../../row/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


