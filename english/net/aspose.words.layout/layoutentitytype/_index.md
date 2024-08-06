---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.LayoutEntityType enum. Types of the layout entities in C#.
type: docs
weight: 3600
url: /net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Types of the layout entities.

```csharp
[Flags]
public enum LayoutEntityType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Default value. |
| Page | `1` | Represents page of a document. Page may have Column, HeaderFooter and Comment child entities. |
| Column | `2` | Represents a column of text on a page. Column may have the same child entities as Cell, plus Footnote, Endnote and NoteSeparator entities. |
| Row | `8` | Represents a table row. Row may have Cell as child entities. |
| Cell | `10` | Represents a table cell. Cell may have Line and Row child entities. |
| Line | `20` | Represents line of characters of text and inline objects. Line may have Span child entities. |
| Span | `40` | Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. Span may not have child entities. |
| Footnote | `100` | Represents placeholder for footnote content. Footnote may have Note child entities. |
| Endnote | `200` | Represents placeholder for endnote content. Endnote may have Note child entities. |
| Note | `4000` | Represents placeholder for note content. Note may have Line and Row child entities. |
| HeaderFooter | `400` | Represents placeholder for header/footer content on a page. HeaderFooter may have Line and Row child entities. |
| TextBox | `800` | Represents text area inside of a shape. Textbox may have Line and Row child entities. |
| Comment | `1000` | Represents placeholder for comment content. Comment may have Line and Row child entities. |
| NoteSeparator | `2000` | Represents footnote/endnote separator. NoteSeparator may have Line and Row child entities. |

## Examples

Shows ways of traversing a document's layout entities.

```csharp
public void LayoutEnumerator()
{
    // Open a document that contains a variety of layout entities.
    // Layout entities are pages, cells, rows, lines, and other objects included in the LayoutEntityType enum.
    // Each layout entity has a rectangular space that it occupies in the document body.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Create an enumerator that can traverse these entities like a tree.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // We can call this method to make sure that the enumerator will be at the first layout entity.
    layoutEnumerator.Reset();

    // There are two orders that determine how the layout enumerator continues traversing layout entities
    // when it encounters entities that span across multiple pages.
    // 1 -  In visual order:
    // When moving through an entity's children that span multiple pages,
    // page layout takes precedence, and we move to other child elements on this page and avoid the ones on the next.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Our enumerator is now at the end of the collection. We can traverse the layout entities backwards to go back to the beginning.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 -  In logical order:
    // When moving through an entity's children that span multiple pages,
    // the enumerator will move between pages to traverse all the child entities.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Enumerate through layoutEnumerator's layout entity collection front-to-back,
/// in a depth-first manner, and in the "Visual" order.
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// Enumerate through layoutEnumerator's layout entity collection back-to-front,
/// in a depth-first manner, and in the "Visual" order.
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// Enumerate through layoutEnumerator's layout entity collection front-to-back,
/// in a depth-first manner, and in the "Logical" order.
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// Enumerate through layoutEnumerator's layout entity collection back-to-front,
/// in a depth-first manner, and in the "Logical" order.
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Print information about layoutEnumerator's current entity to the console, while indenting the text with tab characters
/// based on its depth relative to the root node that we provided in the constructor LayoutEnumerator instance.
/// The rectangle that we process at the end represents the area and location that the entity takes up in the document.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Only spans can contain text.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### See Also

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
