---
title: LayoutEnumerator
second_title: Aspose.Words for C++ API Reference
description: Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of GetEntity() and Current move to the entity which corresponds to a document node.
type: docs
weight: 14
url: /cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of [GetEntity()](../) and [Current](./get_current/) move to the entity which corresponds to a document node.

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Current](./get_current/)() const | Gets or sets current position in the page layout model. This property returns an opaque object which corresponds to the current layout entity. |
| [get_Document](./get_document/)() const | Gets document this instance enumerates. |
| [get_Kind](./get_kind/)() | Gets the kind of the current entity. This can be an empty string but never null. |
| [get_PageIndex](./get_pageindex/)() | Gets the 1-based index of a page which contains the current entity. |
| [get_Rectangle](./get_rectangle/)() | Returns the bounding rectangle of the current entity relative to the page top left corner (in points). |
| [get_Text](./get_text/)() | Gets text of the current span entity. Throws for other entity types. |
| [get_Type](./get_type/)() | Gets the type of the current entity. |
| [idx_get](./idx_get/)(const System::String\&) | Gets a named property of the entity. |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initializes new instance of this class. |
| [MoveFirstChild](./movefirstchild/)() | Moves to the first child entity. |
| [MoveLastChild](./movelastchild/)() | Moves to the last child entity. |
| [MoveNext](./movenext/)() | Moves to the next sibling entity in visual order. When iterating lines of a paragraph broken across pages this method will not move to the next page but rather move to the next entity on the same page. |
| [MoveNextLogical](./movenextlogical/)() | Moves to the next sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the next line even if it resides on another page. |
| [MoveParent](./moveparent/)() | Moves to the parent entity. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Moves to the parent entity of the specified type. |
| [MovePrevious](./moveprevious/)() | Moves to the previous sibling entity. |
| [MovePreviousLogical](./movepreviouslogical/)() | Moves to the previous sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the previous line even if it resides on another page. |
| [Reset](./reset/)() | Moves the enumerator to the first page of the document. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Setter for [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |

## Examples



Shows ways of traversing a document's layout entities. 
```cpp
void LayoutEnumerator_()
{
    // Open a document that contains a variety of layout entities.
    // Layout entities are pages, cells, rows, lines, and other objects included in the LayoutEntityType enum.
    // Each layout entity has a rectangular space that it occupies in the document body.
    auto doc = MakeObject<Document>(MyDir + u"Layout entities.docx");

    // Create an enumerator that can traverse these entities like a tree.
    auto layoutEnumerator = MakeObject<LayoutEnumerator>(doc);

    ASPOSE_ASSERT_EQ(doc, layoutEnumerator->get_Document());

    layoutEnumerator->MoveParent(LayoutEntityType::Page);

    ASSERT_EQ(LayoutEntityType::Page, layoutEnumerator->get_Type());
    ASSERT_THROW(layoutEnumerator->get_Text(), System::InvalidOperationException);

    // We can call this method to make sure that the enumerator will be at the first layout entity.
    layoutEnumerator->Reset();

    // There are two orders that determine how the layout enumerator continues traversing layout entities
    // when it encounters entities that span across multiple pages.
    // 1 -  In visual order:
    // When moving through an entity's children that span multiple pages,
    // page layout takes precedence, and we move to other child elements on this page and avoid the ones on the next.
    std::cout << "Traversing from first to last, elements between pages separated:" << std::endl;
    TraverseLayoutForward(layoutEnumerator, 1);

    // Our enumerator is now at the end of the collection. We can traverse the layout entities backwards to go back to the beginning.
    std::cout << "Traversing from last to first, elements between pages separated:" << std::endl;
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 -  In logical order:
    // When moving through an entity's children that span multiple pages,
    // the enumerator will move between pages to traverse all the child entities.
    std::cout << "Traversing from first to last, elements between pages mixed:" << std::endl;
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    std::cout << "Traversing from last to first, elements between pages mixed:" << std::endl;
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

static void TraverseLayoutForward(SharedPtr<LayoutEnumerator> layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator->MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator->MoveParent();
        }
    } while (layoutEnumerator->MoveNext());
}

static void TraverseLayoutBackward(SharedPtr<LayoutEnumerator> layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator->MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator->MoveParent();
        }
    } while (layoutEnumerator->MovePrevious());
}

static void TraverseLayoutForwardLogical(SharedPtr<LayoutEnumerator> layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator->MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator->MoveParent();
        }
    } while (layoutEnumerator->MoveNextLogical());
}

static void TraverseLayoutBackwardLogical(SharedPtr<LayoutEnumerator> layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator->MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator->MoveParent();
        }
    } while (layoutEnumerator->MovePreviousLogical());
}

static void PrintCurrentEntity(SharedPtr<LayoutEnumerator> layoutEnumerator, int indent)
{
    String tabs(u'\t', indent);

    std::cout << (layoutEnumerator->get_Kind() == String::Empty
                      ? String::Format(u"{0}-> Entity type: {1}", tabs, layoutEnumerator->get_Type())
                      : String::Format(u"{0}-> Entity type & kind: {1}, {2}", tabs, layoutEnumerator->get_Type(), layoutEnumerator->get_Kind()))
              << std::endl;

    // Only spans can contain text.
    if (layoutEnumerator->get_Type() == LayoutEntityType::Span)
    {
        std::cout << tabs << "   Span contents: \"" << layoutEnumerator->get_Text() << "\"" << std::endl;
    }

    System::Drawing::RectangleF leRect = layoutEnumerator->get_Rectangle();
    std::cout << tabs << "   Rectangle dimensions " << leRect.get_Width() << "x" << leRect.get_Height() << ", X=" << leRect.get_X()
              << " Y=" << leRect.get_Y() << std::endl;
    std::cout << tabs << "   Page " << layoutEnumerator->get_PageIndex() << std::endl;
}
```

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words](../../)
