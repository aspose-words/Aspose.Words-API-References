---
title: Aspose::Words::Markup::StructuredDocumentTagCollection::GetById method
linktitle: GetById
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagCollection::GetById method. Returns the structured document tag by identifier in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Returns the structured document tag by identifier.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Parameter | Type | Description |
| --- | --- | --- |
| id | int32_t | The structured document tag identifier. |
## Remarks


Returns null if the structured document tag with the specified identifier cannot be found.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
