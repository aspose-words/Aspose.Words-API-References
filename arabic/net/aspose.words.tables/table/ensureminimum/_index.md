---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Table EnsureMinimum، وقم بإنشاء صف وإضافته بسهولة عندما يكون جدولك فارغًا لإدارة البيانات بسلاسة.
type: docs
weight: 420
url: /ar/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

إذا لم يكن للجدول صفوف، يتم إنشاء صف وإضافته[`Row`](../../row/) .

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
// مع العناصر النموذجية مثل التشغيلات والأشكال وحتى الجداول الأخرى.
// لا يحتوي جدولنا الجديد على أي من هذه العقد، ولا يمكننا إضافة محتويات إليه حتى يحتويها.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// سيؤدي استدعاء طريقة "EnsureMinimum" على جدول إلى ضمان ذلك
//يحتوي الجدول على صف واحد على الأقل وخلية واحدة تحتوي على فقرة فارغة.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
