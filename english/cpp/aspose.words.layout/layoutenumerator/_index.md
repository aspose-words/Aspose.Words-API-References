---
title: Aspose::Words::Layout::LayoutEnumerator class
linktitle: LayoutEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutEnumerator class. Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of GetEntity() and Current move to the entity which corresponds to a document node. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of [GetEntity()](../) and [Current](./get_current/) move to the entity which corresponds to a document node. To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) documentation article.

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Methods

| Method | Description |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Gets or sets current position in the page layout model. This property returns an opaque object which corresponds to the current layout entity. |
| [get_Document](./get_document/)() const | Gets document this instance enumerates. |
| [get_Kind](./get_kind/)() | Gets the kind of the current entity. This can be an empty string but never **null**. |
| [get_PageIndex](./get_pageindex/)() | Gets the 1-based index of a page which contains the current entity. |
| [get_Rectangle](./get_rectangle/)() | Returns the bounding rectangle of the current entity relative to the page top left corner (in points). |
| [get_Text](./get_text/)() | Gets text of the current span entity. Throws for other entity types. |
| [get_Type](./get_type/)() | Gets the type of the current entity. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Gets a named property of the entity. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
