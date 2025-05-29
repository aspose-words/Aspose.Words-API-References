---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نوع PreferredWidth، التي تحدد وحدة القياس لقيم العرض المفضلة، مما يعزز دقة التصميم ومرونته.
type: docs
weight: 40
url: /ar/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

يحصل على وحدة القياس المستخدمة لقيمة العرض المفضلة هذه.

```csharp
public PreferredWidthType Type { get; }
```

## أمثلة

يوضح كيفية التحقق من نوع العرض وقيمة خلية الجدول المفضلة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### أنظر أيضا

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
