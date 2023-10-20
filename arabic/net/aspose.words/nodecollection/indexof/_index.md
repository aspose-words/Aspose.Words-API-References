---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words لـ .NET
description: NodeCollection IndexOf طريقة. إرجاع الفهرس الصفري للعقدة المحددة في C#.
type: docs
weight: 70
url: /ar/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

إرجاع الفهرس الصفري للعقدة المحددة.

```csharp
public int IndexOf(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | العقدة لتحديد موقع. |

### قيمة الإرجاع

الفهرس الصفري للعقدة داخل المجموعة، إذا تم العثور عليه؛ وإلا -1.

## ملاحظات

تقوم هذه الطريقة بإجراء بحث خطي؛ ولذلك فإن متوسط وقت التنفيذ يتناسب مع[`Count`](../count/).

## أمثلة

يوضح كيفية الحصول على فهرس العقدة في المجموعة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### أنظر أيضا

* class [Node](../../node/)
* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
