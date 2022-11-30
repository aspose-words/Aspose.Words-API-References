---
title: get_IsMoveFromRevision
second_title: Aspose.Words for C++ API Reference
description: Returns true if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
type: docs
weight: 404
url: /cpp/aspose.words.drawing/shapebase/get_ismovefromrevision/
---
## ShapeBase::get_IsMoveFromRevision method


Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision()
```


## Examples



Shows how to identify move revision shapes. 
```cpp
// A move revision is when we move an element in the document body by cut-and-pasting it in Microsoft Word while
// tracking changes. If we involve an inline shape in such a text movement, that shape will also be a revision.
// Copying-and-pasting or moving floating shapes do not create move revisions.
auto doc = MakeObject<Document>(MyDir + u"Revision shape.docx");

// Move revisions consist of pairs of "Move from", and "Move to" revisions. We moved in this document in one shape,
// but until we accept or reject the move revision, there will be two instances of that shape.
ArrayPtr<SharedPtr<Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// This is the "Move to" revision, which is the shape at its arrival destination.
// If we accept the revision, this "Move to" revision shape will disappear,
// and the "Move from" revision shape will remain.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// This is the "Move from" revision, which is the shape at its original location.
// If we accept the revision, this "Move from" revision shape will disappear,
// and the "Move to" revision shape will remain.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
