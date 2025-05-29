---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: حسّن بنية خلاياك باستخدام طريقة EnsureMinimum، وأضف فقرة بسهولة إذا لم يكن العنصر الأخير منها. حسّن وضوح مستندك!
type: docs
weight: 160
url: /ar/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

إذا لم يكن الطفل الأخير فقرة، يتم إنشاء فقرة فارغة وإضافتها.

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
// لا تحتوي الخلية الجديدة على أي فقرات، ولا يمكننا إضافة محتويات مثل عقد التشغيل والشكل إليها حتى تحتوي على فقرات.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// سيؤدي استدعاء طريقة "EnsureMinimum" على خلية إلى ضمان ذلك
// تحتوي الخلية على فقرة فارغة واحدة على الأقل، والتي يمكننا بعد ذلك إضافة المحتويات إليها.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Cell](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
