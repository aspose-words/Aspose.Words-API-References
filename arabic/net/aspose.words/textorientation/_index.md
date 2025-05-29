---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.TextOrientation enum للتحكم بسهولة في محاذاة النص في خلايا الجدول وإطارات النص، مما يعزز عرض المستند وقابليته للقراءة.
type: docs
weight: 7280
url: /ar/net/aspose.words/textorientation/
---
## TextOrientation enumeration

يحدد اتجاه النص على الصفحة أو في خلية جدول أو إطار نص.

```csharp
public enum TextOrientation
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Horizontal | `0` | تم ترتيب النص أفقيًا (lr-tb). |
| Downward | `1` | يتم تدوير النص بمقدار 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl). |
| Upward | `3` | يتم تدوير النص بمقدار 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr). |
| HorizontalRotatedFarEast | `4` | يتم ترتيب النص أفقيًا، ولكن يتم تدوير أحرف الشرق الأقصى بمقدار 90 درجة إلى اليسار (lr-tb-v). |
| VerticalFarEast | `5` | تظهر أحرف الشرق الأقصى بشكل عمودي، ويتم تدوير النص الآخر بمقدار 90 درجة إلى اليمين لتظهر من أعلى إلى أسفل (tb-rl-v). |
| VerticalRotatedFarEast | `7` | تظهر أحرف الشرق الأقصى بشكل عمودي، ويتم تدوير النص الآخر بمقدار 90 درجة إلى اليمين لتظهر من أعلى إلى أسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v). |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
