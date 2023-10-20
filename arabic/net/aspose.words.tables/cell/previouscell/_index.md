---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words لـ .NET
description: Cell PreviousCell ملكية. يحصل على السابقCell العقدة في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

يحصل على السابق[`Cell`](../) العقدة

```csharp
public Cell PreviousCell { get; }
```

## ملاحظات

يمكن استخدام هذه الطريقة عندما تحتاج إلى الوصول إلى خلايا a[`Row`](../../row/) . إذا كان a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) تم العثور على العقدة في صف بدلاً من خلية، ويتم اجتيازها تلقائيًا للحصول على خلية موجودة بداخلها.

## أمثلة

يوضح كيفية تعداد جميع خلايا الجدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// تعداد جميع خلايا الجدول.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### أنظر أيضا

* class [Cell](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
