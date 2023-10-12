---
title: CellFormat.Borders
second_title: Aspose.Words لمراجع .NET API
description: CellFormat ملكية. الحصول على مجموعة حدود الخلية.
type: docs
weight: 10
url: /ar/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

الحصول على مجموعة حدود الخلية.

```csharp
public BorderCollection Borders { get; }
```

### أمثلة

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

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../cellformat/)
* المجسم [Aspose.Words](../../../)


