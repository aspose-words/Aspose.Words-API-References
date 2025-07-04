---
title: Aspose::Words::Markup::StructuredDocumentTagCollection class
linktitle: StructuredDocumentTagCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagCollection class. A collection of IStructuredDocumentTag instances that represent the structured document tags in the specified range. To learn more, visit the  documentation article in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


A collection of [IStructuredDocumentTag](../istructureddocumenttag/) instances that represent the structured document tags in the specified range. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() | Returns the number of structured document tags in the collection. |
| [GetById](./getbyid/)(int32_t) | Returns the structured document tag by identifier. |
| [GetByTag](./getbytag/)(const System::String\&) | Returns the first structured document tag encountered in the collection with the specified tag. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Returns the first structured document tag encountered in the collection with the specified title. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns the structured document tag at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Removes the structured document tag with the specified identifier. |
| [RemoveAt](./removeat/)(int32_t) | Removes a structured document tag at the specified index. |
| static [Type](./type/)() |  |

## Examples



Shows how to get structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Get the structured document tag by Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Get the structured document tag or ranged tag by Title.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
