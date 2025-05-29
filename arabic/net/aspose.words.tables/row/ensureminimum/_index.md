---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Row EnsureMinimum، وقم بإنشاء خلية وإضافتها بسهولة عندما لا تكون موجودة، مما يعزز إدارة بنية البيانات لديك.
type: docs
weight: 150
url: /ar/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

إذا كان[`Row`](../) لا يحتوي على خلايا، بل ينشئ ويضيف واحدة[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## أمثلة

يوضح كيفية التأكد من أن عقدة الصف تحتوي على العقد التي نحتاجها لبدء إضافة المحتوى إليها.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// تحتوي الصفوف على خلايا تحتوي على فقرات تحتوي على عناصر نموذجية مثل المسارات والأشكال وحتى الجداول الأخرى.
// لا يحتوي صفنا الجديد على أي من هذه العقد، ولا يمكننا إضافة محتويات إليه حتى يحتوي على هذه العقد.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// سيؤدي استدعاء طريقة "EnsureMinimum" على جدول إلى ضمان ذلك
//يحتوي الجدول على خلية واحدة على الأقل تحتوي على فقرة فارغة.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
