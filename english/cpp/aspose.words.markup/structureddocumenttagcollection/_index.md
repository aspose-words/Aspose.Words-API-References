---
title: StructuredDocumentTagCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of IStructuredDocumentTag instances that represent the structured document tags in the specified range.
type: docs
weight: 144
url: /cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


A collection of [IStructuredDocumentTag](../istructureddocumenttag/) instances that represent the structured document tags in the specified range.

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
| [idx_get](./idx_get/)(int32_t) | Returns the structured document tag at the specified index. |
| [Remove](./remove/)(int32_t) | Removes the structured document tag with the specified identifier. |
| [RemoveAt](./removeat/)(int32_t) | Removes a structured document tag at the specified index. |
## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words](../../)
