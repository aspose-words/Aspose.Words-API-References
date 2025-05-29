---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsColumn. حدّد بسهولة ما إذا كانت الإشارة المرجعية تُمثّل عمودًا في جدول، مما يُحسّن من سهولة التنقل في مستنداتك وتنظيمها.
type: docs
weight: 40
url: /ar/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

إرجاع`حقيقي` إذا كانت هذه الإشارة المرجعية عبارة عن إشارة مرجعية لعمود جدول.

```csharp
public bool IsColumn { get; }
```

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
