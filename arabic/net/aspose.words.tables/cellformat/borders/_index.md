---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية حدود تنسيق الخلية للوصول إلى مجموعات حدود الخلية وتخصيصها لتحسين تصميم جداول البيانات ووظائفها.
type: docs
weight: 10
url: /ar/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

يحصل على مجموعة من حدود الخلية.

```csharp
public BorderCollection Borders { get; }
```

## أمثلة

يوضح كيفية دمج الصفوف من جدولين في جدول واحد.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// فيما يلي طريقتان للحصول على جدول من مستند.
// 1 - من مجموعة "الجداول" لعقدة الجسم:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - استخدام طريقة "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

//إضافة كافة الصفوف من الجدول الحالي إلى الجدول التالي.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// قم بإزالة حاوية الجدول الفارغة.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### أنظر أيضا

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
