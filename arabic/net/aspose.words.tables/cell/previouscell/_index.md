---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول بسهولة إلى عقدة الخلية السابقة باستخدام خاصية "الخلية السابقة". حسّن تصفح بياناتك وسهّل عملية الترميز.
type: docs
weight: 110
url: /ar/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

يحصل على السابق[`Cell`](../) العقدة.

```csharp
public Cell PreviousCell { get; }
```

## ملاحظات

يمكن استخدام الطريقة عندما تحتاج إلى الوصول إلى خلايا مكتوبة[`Row`](../../row/) . إذا a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) إذا تم العثور على العقدة في صف بدلاً من خلية، فسيتم اجتيازها تلقائيًا للحصول على خلية موجودة داخلها.

## أمثلة

يوضح كيفية ترقيم جميع خلايا الجدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

//إحصاء جميع خلايا الجدول.
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
