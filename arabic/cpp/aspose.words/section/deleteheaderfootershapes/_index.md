---
title: "طريقة Aspose::Words::Section::DeleteHeaderFooterShapes"
linktitle: "DeleteHeaderFooterShapes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::DeleteHeaderFooterShapes. تحذف جميع الأشكال (كائنات الرسم) من رؤوس وتذييلات هذا القسم في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


يحذف جميع الأشكال (كائنات الرسم) من رؤوس وتذييلات هذا القسم.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## أمثلة



يظهر كيفية إزالة جميع الأشكال من جميع رؤوس وتذييلات القسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء رأس أساسي مع شكل.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// إنشاء تذييل أساسي مع صورة.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// إزالة جميع الأشكال من الرؤوس والتذييلات في القسم الأول.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## انظر أيضًا

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
