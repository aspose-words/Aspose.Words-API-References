---
title: LayoutEntityType enumeration
linktitle: LayoutEntityType enumeration
articleTitle: LayoutEntityType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Layout.LayoutEntityType enumeration. Types of the layout entities."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Layout/layoutentitytype/
---

## LayoutEntityType enumeration

Types of the layout entities.


### Members

| Name | Description |
| --- | --- |
| None | Default value. |
| Page | Represents page of a document. |
| Column | Represents a column of text on a page. |
| Row | Represents a table row. |
| Cell | Represents a table cell. |
| Line | Represents line of characters of text and inline objects. |
| Span | Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. |
| Footnote | Represents placeholder for footnote content. |
| Endnote | Represents placeholder for endnote content. |
| Note | Represents placeholder for note content. |
| HeaderFooter | Represents placeholder for header/footer content on a page. |
| TextBox | Represents text area inside of a shape. |
| Comment | Represents placeholder for comment content. |
| NoteSeparator | Represents footnote/endnote separator. |

### Examples

Shows ways of traversing a document's layout entities.

```js
test('LayoutEnumerator', () => {
  // Open a document that contains a variety of layout entities.
  // Layout entities are pages, cells, rows, lines, and other objects included in the LayoutEntityType enum.
  // Each layout entity has a rectangular space that it occupies in the document body.
  let doc = new aw.Document(base.myDir + "Layout entities.docx");

  // Create an enumerator that can traverse these entities like a tree.
  let layoutEnumerator = new aw.Layout.LayoutEnumerator(doc);

  expect(layoutEnumerator.document).toEqual(doc);

  layoutEnumerator.moveParent(aw.Layout.LayoutEntityType.Page);

  expect(layoutEnumerator.type).toEqual(aw.Layout.LayoutEntityType.Page);
  expect(() => console.log(layoutEnumerator.text)).toThrow("Operation is not valid due to the current state of the object.");

  // We can call this method to make sure that the enumerator will be at the first layout entity.
  layoutEnumerator.reset();

  // There are two orders that determine how the layout enumerator continues traversing layout entities
  // when it encounters entities that span across multiple pages.
  // 1 -  In visual order:
  // When moving through an entity's children that span multiple pages,
  // page layout takes precedence, and we move to other child elements on this page and avoid the ones on the next.
  console.log("Traversing from first to last, elements between pages separated:");
  TraverseLayoutForward(layoutEnumerator, 1);

  // Our enumerator is now at the end of the collection. We can traverse the layout entities backwards to go back to the beginning.
  console.log("Traversing from last to first, elements between pages separated:");
  TraverseLayoutBackward(layoutEnumerator, 1);

  // 2 -  In logical order:
  // When moving through an entity's children that span multiple pages,
  // the enumerator will move between pages to traverse all the child entities.
  console.log("Traversing from first to last, elements between pages mixed:");
  TraverseLayoutForwardLogical(layoutEnumerator, 1);

  console.log("Traversing from last to first, elements between pages mixed:");
  TraverseLayoutBackwardLogical(layoutEnumerator, 1);
});


  /// <summary>
  /// Enumerate through layoutEnumerator's layout entity collection front-to-back,
  /// in a depth-first manner, and in the "Visual" order.
  /// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
  do
  {
    PrintCurrentEntity(layoutEnumerator, depth);

    if (layoutEnumerator.moveFirstChild())
    {
      TraverseLayoutForward(layoutEnumerator, depth + 1);
      layoutEnumerator.moveParent();
    }
  } while (layoutEnumerator.moveNext());
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

    if (layoutEnumerator.moveLastChild())
    {
      TraverseLayoutBackward(layoutEnumerator, depth + 1);
      layoutEnumerator.moveParent();
    }
  } while (layoutEnumerator.movePrevious());
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

    if (layoutEnumerator.moveFirstChild())
    {
      TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
      layoutEnumerator.moveParent();
    }
  } while (layoutEnumerator.moveNextLogical());
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

    if (layoutEnumerator.moveLastChild())
    {
      TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
      layoutEnumerator.moveParent();
    }
  } while (layoutEnumerator.movePreviousLogical());
}

  /// <summary>
  /// Print information about layoutEnumerator's current entity to the console, while indenting the text with tab characters
  /// based on its depth relative to the root node that we provided in the constructor LayoutEnumerator instance.
  /// The rectangle that we process at the end represents the area and location that the entity takes up in the document.
  /// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
  let tabs = new string('\t', indent);

  console.log(layoutEnumerator.kind == ''
    ? `${tabs}-> Entity type: ${layoutEnumerator.type}`
    : `${tabs}-> Entity type & kind: ${layoutEnumerator.type}, ${layoutEnumerator.kind}`);

    // Only spans can contain text.
  if (layoutEnumerator.type == aw.Layout.LayoutEntityType.Span)
    console.log(`${tabs}   Span contents: \"${layoutEnumerator.text}\"`);

  RectangleF leRect = layoutEnumerator.rectangle;
  console.log(`${tabs}   Rectangle dimensions ${leRect.width}x${leRect.height}, X=${leRect.X} Y=${leRect.Y}`);
  console.log(`${tabs}   Page ${layoutEnumerator.pageIndex}`);
}
```

### See Also

* module [Aspose.Words.Layout](../)

