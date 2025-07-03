---
title: Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection method
linktitle: get_IsMultiSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection method. Returns true if this instance is a ranged (multi-section) structured document tag in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Returns true if this instance is a ranged (multi-section) structured document tag.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
