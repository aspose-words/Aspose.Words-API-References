---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words لـ .NET
description: Row IsLastRow ملكية. صحيح إذا كان هذا هو الصف الأخير في الجدول كاذبة خلاف ذلك في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

صحيح إذا كان هذا هو الصف الأخير في الجدول؛ كاذبة خلاف ذلك.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
