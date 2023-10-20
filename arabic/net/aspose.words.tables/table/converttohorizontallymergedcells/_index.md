---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words لـ .NET
description: Table ConvertToHorizontallyMergedCells طريقة. تحويل الخلايا المدمجة أفقيا حسب العرض إلى الخلايا المدمجة بهاHorizontalMerge  في C#.
type: docs
weight: 390
url: /ar/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

تحويل الخلايا المدمجة أفقيا حسب العرض إلى الخلايا المدمجة بها[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## ملاحظات

يمكن دمج خلايا الجدول أفقيًا إما باستخدام علامات الدمج[`HorizontalMerge`](../../cellformat/horizontalmerge/) أو باستخدام عرض الخلية[`Width`](../../cellformat/width/).

عندما يتم دمج خلية الجدول بواسطة خاصية العرض[`HorizontalMerge`](../../cellformat/horizontalmerge/) لا معنى له ولكن في بعض الأحيان يكون وجود علامات الدمج طريقة أكثر ملاءمة.

استخدم هذه الطريقة لتحويل خلايا الجدول المدمجة أفقيًا حسب العرض إلى خلايا مدمجة بواسطة إشارات الدمج.

## أمثلة

يوضح كيفية تحويل الخلايا المدمجة أفقياً حسب العرض إلى خلايا مدمجة بواسطة CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// لم يعد Microsoft Word يكتب علامات الدمج بعد الآن، بل يحدد الخلايا المدمجة حسب العرض بدلاً من ذلك.
// يحدد Aspose.Words بشكل افتراضي 5 خلايا فقط في الصف، ولا تحتوي أي منها على علامة الدمج الأفقي،
// على الرغم من وجود 7 خلايا في الصف قبل حدوث الدمج الأفقي.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// استخدم طريقة "ConvertToHorizontallyMergedCells" لتحويل الخلايا المدمجة أفقيًا
// حسب عرضه للخلية المدمجة أفقيًا بواسطة الأعلام.
// الآن، لدينا 7 خلايا، وبعضها يحتوي على قيم دمج أفقي.
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
