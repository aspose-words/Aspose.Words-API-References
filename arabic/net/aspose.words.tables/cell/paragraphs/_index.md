---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية فقرات الخلية للوصول إلى مجموعة من فقرات الأطفال المباشرة، مما يعزز بنية مستندك وقابليته للقراءة.
type: docs
weight: 90
url: /ar/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

يحصل على مجموعة من الفقرات التي تعتبر أبناءً مباشرين للخلية.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
