---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: Table EnsureMinimum طريقة. إذا لم يكن الجدول يحتوي على صفوف فسيتم إنشاء واحد وإلحاقهRow  في C#.
type: docs
weight: 400
url: /ar/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

إذا لم يكن الجدول يحتوي على صفوف، فسيتم إنشاء واحد وإلحاقه[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## أمثلة

يوضح كيفية التأكد من أن عقدة الجدول تحتوي على العقد التي نحتاجها لإضافة المحتوى.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// تحتوي الجداول على صفوف تحتوي على خلايا قد تحتوي على فقرات
// مع عناصر نموذجية مثل المسارات والأشكال وحتى الجداول الأخرى.
// لا يحتوي جدولنا الجديد على أي من هذه العقد، ولا يمكننا إضافة محتويات إليه حتى يتم ذلك.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// سيؤدي استدعاء طريقة "EnsureMinimum" على الجدول إلى التأكد من ذلك
// يحتوي الجدول على صف واحد على الأقل وخلية واحدة بها فقرة فارغة.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
