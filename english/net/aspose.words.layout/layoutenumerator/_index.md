---
title: Class LayoutEnumerator
second_title: Aspose.Words for .NET API Reference
description: Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type geometry text and page index where entity is rendered as well as overall structure and relationships. Use combination of GetEntity and Current move to the entity which corresponds to a document node in C#
type: docs
weight: 3160
url: /net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of [`GetEntity`](../layoutcollector/getentity/) and [`Current`](./current/) move to the entity which corresponds to a document node.

To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) documentation article.

```csharp
public class LayoutEnumerator
```

## Constructors

| Name | Description |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(Document) | Initializes new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Gets or sets current position in the page layout model. This property returns an opaque object which corresponds to the current layout entity. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Gets document this instance enumerates. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Gets a named property of the entity. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Gets the kind of the current entity. This can be an empty string but never `null`. |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Gets the 1-based index of a page which contains the current entity. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Returns the bounding rectangle of the current entity relative to the page top left corner (in points). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Gets text of the current span entity. Throws for other entity types. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Gets the type of the current entity. |

## Methods

| Name | Description |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Moves to the first child entity. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Moves to the last child entity. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Moves to the next sibling entity in visual order. When iterating lines of a paragraph broken across pages this method will not move to the next page but rather move to the next entity on the same page. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Moves to the next sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the next line even if it resides on another page. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Moves to the parent entity. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(LayoutEntityType) | Moves to the parent entity of the specified type. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Moves to the previous sibling entity. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Moves to the previous sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the previous line even if it resides on another page. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Moves the enumerator to the first page of the document. |

## Examples

Shows ways of traversing a document's layout entities.

```csharp
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
