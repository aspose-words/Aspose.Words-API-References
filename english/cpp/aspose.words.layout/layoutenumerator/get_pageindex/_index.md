---
title: get_PageIndex
second_title: Aspose.Words for C++ API Reference
description: Gets the 1-based index of a page which contains the current entity.
type: docs
weight: 53
url: /cpp/aspose.words.layout/layoutenumerator/get_pageindex/
---
## LayoutEnumerator::get_PageIndex method


Gets the 1-based index of a page which contains the current entity.

```cpp
int32_t Aspose::Words::Layout::LayoutEnumerator::get_PageIndex()
```


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

* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words](../../../)
