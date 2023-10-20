---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words لـ .NET
description: PreferredWidth Value ملكية. يحصل على قيمة العرض المفضلة. وحدة القياس محددة فيType الملكية في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

يحصل على قيمة العرض المفضلة. وحدة القياس محددة في[`Type`](../type/) الملكية.

```csharp
public double Value { get; }
```

## أمثلة

يوضح كيفية التحقق من نوع العرض المفضل وقيمة خلية الجدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### أنظر أيضا

* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
