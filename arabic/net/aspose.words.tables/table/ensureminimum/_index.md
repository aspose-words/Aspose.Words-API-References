---
title: Table.EnsureMinimum
second_title: Aspose.Words لمراجع .NET API
description: Table طريقة. في حالة عدم احتواء الجدول على صفوف  يتم إنشاء صفوف وإلحاقها صف .
type: docs
weight: 400
url: /ar/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

في حالة عدم احتواء الجدول على صفوف ، يتم إنشاء صفوف وإلحاقها **صف** .

```csharp
public void EnsureMinimum()
```

### أمثلة

يوضح كيفية التأكد من احتواء عقدة الجدول على العقد التي نحتاجها لإضافة محتوى.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// تحتوي الجداول على صفوف تحتوي على خلايا قد تحتوي على فقرات
// مع عناصر نموذجية مثل المسارات والأشكال وحتى الجداول الأخرى.
// لا يحتوي جدولنا الجديد على أي من هذه العقد ، ولا يمكننا إضافة محتويات إليه حتى يحدث ذلك.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// استدعاء طريقة "ضمان الحد الأدنى" على الطاولة سيضمن ذلك
// يحتوي الجدول على صف واحد على الأقل وخلية واحدة تحتوي على فقرة فارغة.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


