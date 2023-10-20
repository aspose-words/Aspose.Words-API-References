---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: Cell EnsureMinimum طريقة. إذا لم يكن العنصر الفرعي الأخير فقرة فسيتم إنشاء فقرة واحدة فارغة وإلحاقها في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

إذا لم يكن العنصر الفرعي الأخير فقرة، فسيتم إنشاء فقرة واحدة فارغة وإلحاقها.

```csharp
public void EnsureMinimum()
```

## أمثلة

يوضح كيفية التأكد من أن عقدة الخلية تحتوي على العقد التي نحتاجها لبدء إضافة المحتوى إليها.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// قد تحتوي الخلايا على فقرات تحتوي على عناصر نموذجية مثل المسارات والأشكال وحتى الجداول الأخرى.
// لا تحتوي خليتنا الجديدة على أي فقرات، ولا يمكننا إضافة محتويات مثل عقد التشغيل والشكل إليها حتى تحتوي عليها.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// سيؤدي استدعاء طريقة "EnsureMinimum" على الخلية إلى التأكد من ذلك
// تحتوي الخلية على فقرة فارغة واحدة على الأقل، والتي يمكننا بعد ذلك إضافة محتويات إليها.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Cell](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
