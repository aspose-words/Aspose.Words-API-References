---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: Row EnsureMinimum طريقة. إذاRow لا يحتوي على خلايا ويقوم بإنشاء وإلحاق واحدةCell  في C#.
type: docs
weight: 130
url: /ar/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

إذا[`Row`](../) لا يحتوي على خلايا، ويقوم بإنشاء وإلحاق واحدة[`Cell`](../../cell/) .

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
// لا يحتوي صفنا الجديد على أي من هذه العقد، ولا يمكننا إضافة محتويات إليه حتى يتم ذلك.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// سيؤدي استدعاء طريقة "EnsureMinimum" على الجدول إلى التأكد من ذلك
// يحتوي الجدول على خلية واحدة على الأقل تحتوي على فقرة فارغة.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
