---
title: Cell.ParentRow
second_title: Aspose.Words لمراجع .NET API
description: Cell ملكية. إرجاع الصف الأصلي للخلية.
type: docs
weight: 100
url: /ar/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

إرجاع الصف الأصلي للخلية.

```csharp
public Row ParentRow { get; }
```

### ملاحظات

أي ما يعادلFirstNonMarkupParentNode يلقي ل[`Row`](../../row/).

### أمثلة

يوضح كيفية إعداد جدول للبقاء معًا في نفس الصفحة.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// تمكين KeepWithNext لكل فقرة في الجدول باستثناء فقرة
// آخر العناصر الموجودة في الصف الأخير ستمنع تقسيم الجدول عبر صفحات متعددة.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### أنظر أيضا

* class [Row](../../row/)
* class [Cell](../)
* مساحة الاسم [Aspose.Words.Tables](../../cell/)
* المجسم [Aspose.Words](../../../)


