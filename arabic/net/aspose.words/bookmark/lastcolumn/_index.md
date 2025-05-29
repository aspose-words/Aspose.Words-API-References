---
title: Bookmark.LastColumn
linktitle: LastColumn
articleTitle: LastColumn
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LastColumn، وتمكن من الوصول بسهولة إلى الفهرس المبدئي للعمود الأخير في نطاق الإشارة المرجعية للجدول الخاص بك لإدارة البيانات بكفاءة.
type: docs
weight: 50
url: /ar/net/aspose.words/bookmark/lastcolumn/
---
## Bookmark.LastColumn property

يحصل على الفهرس المبني على الصفر للعمود الأخير من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية.

```csharp
public int LastColumn { get; }
```

## ملاحظات

إرجاع**-1** إذا لم تكن هذه الإشارة المرجعية إشارة مرجعية لعمود جدول.

## أمثلة

يوضح كيفية الحصول على معلومات حول إشارات مرجعية لأعمدة الجدول.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // إذا كانت الإشارة المرجعية تحتوي على أعمدة جدول، فهي إشارة مرجعية لأعمدة الجدول، ويتم تعيين علم IsColumn الخاص بها على true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // اطبع محتويات العمود الأول والأخير المحيط بالإشارة المرجعية.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### أنظر أيضا

* class [Bookmark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
