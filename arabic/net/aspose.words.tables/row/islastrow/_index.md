---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Row IsLastRow. حدّد بسهولة ما إذا كان الصف هو الأخير في الجدول، مما يُسهّل إدارة البيانات ويحسّن كفاءة البرمجة.
type: docs
weight: 50
url: /ar/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

صحيح إذا كان هذا هو الصف الأخير في الجدول؛ وإلا يكون خطأ.

```csharp
public bool IsLastRow { get; }
```

## أمثلة

يوضح كيفية إعداد جدول للبقاء معًا على نفس الصفحة.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// تمكين KeepWithNext لكل فقرة في الجدول باستثناء
// آخر العناصر الموجودة في الصف الأخير ستمنع الجدول من الانقسام عبر صفحات متعددة.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### أنظر أيضا

* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
