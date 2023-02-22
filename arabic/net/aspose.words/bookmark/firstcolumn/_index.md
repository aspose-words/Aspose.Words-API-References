---
title: Bookmark.FirstColumn
second_title: Aspose.Words لمراجع .NET API
description: Bookmark ملكية. الحصول على الفهرس الصفري للعمود الأول من نطاق عمود الجدول المرتبط بالإشارة المرجعية.
type: docs
weight: 30
url: /ar/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

الحصول على الفهرس الصفري للعمود الأول من نطاق عمود الجدول المرتبط بالإشارة المرجعية.

```csharp
public int FirstColumn { get; }
```

### ملاحظات

عوائد **-1** إذا كانت هذه الإشارة المرجعية ليست إشارة مرجعية لعمود الجدول.

### أمثلة

يوضح كيفية الحصول على معلومات حول الإشارات المرجعية لأعمدة الجدول.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // إذا كانت الإشارة المرجعية تضم أعمدة في الجدول ، فهي إشارة مرجعية لعمود الجدول ، ويتم تعيين علامة IsColumn الخاصة بها على صحيح.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // طباعة محتويات العمودين الأول والأخير المحاطين بالإشارة المرجعية.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### أنظر أيضا

* class [Bookmark](../)
* مساحة الاسم [Aspose.Words](../../bookmark/)
* المجسم [Aspose.Words](../../../)


