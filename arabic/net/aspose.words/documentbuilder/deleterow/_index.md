---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words لـ .NET
description: احذف الصفوف من الجداول بسهولة باستخدام طريقة DeleteRow في DocumentBuilder. حسّن عملية تحرير مستنداتك وحسّن سير عملك!
type: docs
weight: 200
url: /ar/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

يحذف صفًا من جدول.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableIndex | Int32 | فهرس الجدول. |
| rowIndex | Int32 | مؤشر الصف في الجدول. |

### قيمة الإرجاع

عقدة الصف التي تمت إزالتها للتو.

## ملاحظات

إذا كان المؤشر داخل الصف الذي يتم حذفه، يتم نقل المؤشر إلى الصف التالي أو إلى الفقرة التالية بعد الجدول.

إذا قمت بحذف صف من جدول يحتوي على صف واحد فقط، فسيتم حذف الجدول whole .

بالنسبة لمعلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، يُحدد فهرس from في البداية، حيث يكون 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، يُحدد فهرس from في النهاية، حيث يكون -1 هو العنصر الأخير.

## أمثلة

يوضح كيفية حذف صف من جدول.

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

//حذف الصف الأول من الجدول الأول في المستند.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### أنظر أيضا

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
