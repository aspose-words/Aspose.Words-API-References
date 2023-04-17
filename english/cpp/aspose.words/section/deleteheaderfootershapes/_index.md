---
title: Aspose::Words::Section::DeleteHeaderFooterShapes method
linktitle: DeleteHeaderFooterShapes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section::DeleteHeaderFooterShapes method. Deletes all shapes (drawing objects) from the headers and footers of this section in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


Deletes all shapes (drawing objects) from the headers and footers of this section.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## Examples



Shows how to remove all shapes from all headers footers in a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a primary header with a shape.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->InsertShape(ShapeType::Rectangle, 100, 100);

// Create a primary footer with an image.
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->InsertImage(ImageDir + u"Logo Icon.ico");

ASSERT_EQ(1,
          doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->GetChildNodes(NodeType::Shape, true)->get_Count());
ASSERT_EQ(1,
          doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->GetChildNodes(NodeType::Shape, true)->get_Count());

// Remove all shapes from the headers and footers in the first section.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0,
          doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->GetChildNodes(NodeType::Shape, true)->get_Count());
ASSERT_EQ(0,
          doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->GetChildNodes(NodeType::Shape, true)->get_Count());
```

## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
