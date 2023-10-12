---
title: CompositeNode.HasChildNodes
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode ملكية. إرجاعحقيقي إذا كانت هذه العقدة تحتوي على أي عقد فرعية.
type: docs
weight: 30
url: /ar/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية.

```csharp
public bool HasChildNodes { get; }
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

* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


