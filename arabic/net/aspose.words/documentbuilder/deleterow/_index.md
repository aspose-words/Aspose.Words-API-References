---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words لـ .NET
description: DocumentBuilder DeleteRow طريقة. حذف صف من الجدول في C#.
type: docs
weight: 200
url: /ar/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

حذف صف من الجدول.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableIndex | Int32 | فهرس الجدول. |
| rowIndex | Int32 | فهرس الصف في الجدول. |

### قيمة الإرجاع

عقدة الصف التي تمت إزالتها للتو.

## ملاحظات

إذا كان المؤشر داخل الصف الذي يتم حذفه، فسيتم نقل المؤشر إلى الصف التالي أو إلى الفقرة التالية بعد الجدول.

إذا قمت بحذف صف من جدول يحتوي على صف واحد فقط، فسيتم حذف الجدول full .

بالنسبة لمعلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، فإنه يحدد فهرس from البداية حيث يكون 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، فإنه يحدد فهرس from النهاية مع -1 كونه العنصر الأخير.

## أمثلة

يوضح كيفية حذف صف من الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// احذف الصف الأول من الجدول الأول في المستند.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### أنظر أيضا

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
