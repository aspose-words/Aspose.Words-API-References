---
title: ParagraphFormat.KeepWithNext
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. صحيح إذا كانت الفقرة ستبقى في نفس الصفحة مثل الفقرة التي تليها.
type: docs
weight: 170
url: /ar/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

صحيح إذا كانت الفقرة ستبقى في نفس الصفحة مثل الفقرة التي تليها.

```csharp
public bool KeepWithNext { get; set; }
```

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

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


