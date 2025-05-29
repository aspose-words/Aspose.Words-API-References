---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "الفقرة في الخلية". حدّد بسهولة ما إذا كانت الفقرة فرعًا مباشرًا لخلية، مما يُحسّن بنية مستندك وتنسيقه.
type: docs
weight: 100
url: /ar/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

صحيح إذا كانت هذه الفقرة طفلًا مباشرًا لـ[`Cell`](../../../aspose.words.tables/cell/) ؛ وإلا فسيكون خاطئًا.

```csharp
public bool IsInCell { get; }
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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
