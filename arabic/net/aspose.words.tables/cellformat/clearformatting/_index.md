---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CellFormat ClearFormatting لإعادة ضبط أنماط الخلايا إلى الوضع الافتراضي بسهولة دون تغيير عرض الخلية. حسّن كفاءة جدول بياناتك!
type: docs
weight: 160
url: /ar/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

يُعيد ضبط تنسيق الخلية الافتراضي. لا يُغيّر عرض الخلية.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
