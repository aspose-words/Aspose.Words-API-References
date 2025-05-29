---
title: CellVerticalAlignment Enum
linktitle: CellVerticalAlignment
articleTitle: CellVerticalAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Tables.CellVerticalAlignment لمحاذاة مثالية للنص في خلايا الجدول. حسّن تصميم مستندك بسهولة!
type: docs
weight: 7130
url: /ar/net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

يحدد محاذاة رأسية للنص داخل خلية الجدول.

```csharp
public enum CellVerticalAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Top | `0` | تم محاذاة النص في الجزء العلوي من الخلية. |
| Center | `1` | تم محاذاة النص في منتصف الخلية. |
| Bottom | `2` | تم محاذاة النص في أسفل الخلية. |

## أمثلة

يوضح كيفية إنشاء جدول 2x2 منسق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// أثناء إنشاء الجدول، سيقوم منشئ المستند بتطبيق قيم خصائص RowFormat/CellFormat الحالية
// إلى الصف/الخلية الحالية التي يتواجد بها المؤشر وأي صفوف/خلايا جديدة أثناء إنشائها.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// لا تتأثر الصفوف والخلايا المضافة مسبقًا بأثر رجعي بالتغييرات التي تطرأ على تنسيق المنشئ.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
