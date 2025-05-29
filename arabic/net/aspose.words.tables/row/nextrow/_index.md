---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية NextRow للوصول بسهولة إلى عقدة الصف التالية، مما يعزز تجربة التنقل وإدارة البيانات لديك.
type: docs
weight: 70
url: /ar/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

يحصل على التالي[`Row`](../) العقدة.

```csharp
public Row NextRow { get; }
```

## ملاحظات

يمكن استخدام هذه الطريقة عند الحاجة إلى الوصول الكتابي إلى صفوف الجدول. إذا كانت a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) تم العثور على العقدة في جدول بدلاً من صف، يتم اجتيازها تلقائيًا للحصول على صف موجود داخلها.

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

* class [Row](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
