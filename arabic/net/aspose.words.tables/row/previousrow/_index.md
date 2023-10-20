---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words لـ .NET
description: Row PreviousRow ملكية. يحصل على السابقRow العقدة في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

يحصل على السابق[`Row`](../) العقدة

```csharp
public Row PreviousRow { get; }
```

## ملاحظات

يمكن استخدام هذه الطريقة عندما تحتاج إلى الوصول إلى صفوف الجدول. إذا كان a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)تم العثور على العقدة في جدول بدلاً من صف، يتم اجتيازها تلقائيًا للحصول على صف موجود بداخله.

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

* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
