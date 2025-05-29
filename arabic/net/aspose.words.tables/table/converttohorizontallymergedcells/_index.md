---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة ConvertToHorizontallyMergedCells بتحويل الخلايا المدمجة العريضة إلى خلايا مدمجة أفقياً، مما يعزز تنظيم البيانات لديك.
type: docs
weight: 410
url: /ar/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

يحول الخلايا المندمجة أفقيًا حسب العرض إلى خلايا مندمجة حسب[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## ملاحظات

يمكن دمج خلايا الجدول أفقيًا باستخدام علامات الدمج[`HorizontalMerge`](../../cellformat/horizontalmerge/) أو باستخدام عرض الخلية[`Width`](../../cellformat/width/).

عندما يتم دمج خلية الجدول بواسطة خاصية العرض[`HorizontalMerge`](../../cellformat/horizontalmerge/) لا معنى له، ولكن في بعض الأحيان يكون وجود أعلام الدمج هو الطريقة الأكثر ملاءمة.

استخدم هذه الطريقة لتحويل خلايا الجدول المدمجة أفقياً حسب العرض إلى خلايا مدمجة بواسطة علامات الدمج.

## أمثلة

يوضح كيفية تحويل الخلايا المدمجة أفقياً حسب العرض إلى خلايا مدمجة بواسطة CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// لم يعد برنامج Microsoft Word يكتب علامات الدمج، بل يقوم بدلاً من ذلك بتحديد الخلايا المدمجة حسب العرض.
// يحدد Aspose.Words بشكل افتراضي 5 خلايا فقط في صف واحد، ولا يحتوي أي منها على علامة الدمج الأفقي،
// على الرغم من وجود 7 خلايا في الصف قبل إجراء الدمج الأفقي.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// استخدم طريقة "ConvertToHorizontallyMergedCells" لتحويل الخلايا المدمجة أفقيًا
// حسب عرضها إلى الخلية المندمجة أفقيًا بواسطة الأعلام.
// الآن، لدينا 7 خلايا، وبعضها يحتوي على قيم دمج أفقية.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
