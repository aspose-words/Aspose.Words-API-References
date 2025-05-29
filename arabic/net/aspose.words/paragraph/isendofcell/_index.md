---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsEndOfCell للفقرات. تعلّم كيفية تحديد ما إذا كانت الفقرة هي الأخيرة في الخلية، مما يُحسّن بنية مستندك.
type: docs
weight: 50
url: /ar/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`Cell`](../../../aspose.words.tables/cell/) ؛ وإلا فسيكون خاطئًا.

```csharp
public bool IsEndOfCell { get; }
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
