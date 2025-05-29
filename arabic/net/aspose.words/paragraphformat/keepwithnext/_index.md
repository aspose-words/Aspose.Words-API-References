---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تضمن خاصية ParagraphFormat KeepWithNext بقاء فقراتك معًا، مما يعزز تدفق المستند وقابلية قراءته للحصول على مظهر أنيق.
type: docs
weight: 170
url: /ar/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

صحيح إذا كانت الفقرة ستبقى على نفس الصفحة مثل الفقرة التي تليها.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
