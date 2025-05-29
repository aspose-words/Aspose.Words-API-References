---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة NodeCollection IndexOf للعثور بكفاءة على الفهرس المبني على الصفر لأي عقدة محددة في مجموعاتك.
type: docs
weight: 70
url: /ar/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

يعيد الفهرس المبني على الصفر للعقدة المحددة.

```csharp
public int IndexOf(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | العقدة التي يجب تحديد موقعها. |

### قيمة الإرجاع

الفهرس المبني على الصفر للعقدة داخل المجموعة، إذا تم العثور عليه؛ وإلا، -1.

## ملاحظات

تقوم هذه الطريقة بإجراء بحث خطي؛ وبالتالي فإن متوسط وقت التنفيذ يتناسب مع[`Count`](../count/).

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
