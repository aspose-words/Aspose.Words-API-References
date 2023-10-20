---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words لـ .NET
description: Paragraph IsInCell ملكية. صحيح إذا كانت هذه الفقرة فرعًا مباشرًا لـCell  كاذبة خلاف ذلك في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

صحيح إذا كانت هذه الفقرة فرعًا مباشرًا لـ[`Cell`](../../../aspose.words.tables/cell/) ; كاذبة خلاف ذلك.

```csharp
public bool IsInCell { get; }
```

## أمثلة

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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
