---
title: Paragraphs
second_title: Aspose.Words لمراجع .NET API
description: الحصول على مجموعة من الفقرات التي تعتبر توابع مباشرة للخلية.
type: docs
weight: 80
url: /ar/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

الحصول على مجموعة من الفقرات التي تعتبر توابع مباشرة للخلية.

```csharp
public ParagraphCollection Paragraphs { get; }
```

### أمثلة

يوضح كيفية إعداد جدول للبقاء معًا في نفس الصفحة.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// تمكين KeepWithNext لكل فقرة في الجدول باستثناء ملف
// الأخيرة في الصف الأخير ستمنع الجدول من الانقسام عبر صفحات متعددة.
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection)
* class [Cell](../../cell)
* مساحة الاسم [Aspose.Words.Tables](../../cell)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->