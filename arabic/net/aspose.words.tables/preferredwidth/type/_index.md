---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: PreferredWidth Type ملكية. للحصول على وحدة القياس المستخدمة لقيمة العرض المفضلة هذه في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

للحصول على وحدة القياس المستخدمة لقيمة العرض المفضلة هذه.

```csharp
public PreferredWidthType Type { get; }
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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
