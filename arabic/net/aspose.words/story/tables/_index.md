---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words لـ .NET
description: Story Tables ملكية. الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/story/tables/
---
## Story.Tables property

الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة.

```csharp
public TableCollection Tables { get; }
```

## أمثلة

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

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
