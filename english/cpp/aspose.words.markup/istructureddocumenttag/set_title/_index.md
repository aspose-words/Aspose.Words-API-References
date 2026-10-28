---
title: Aspose::Words::Markup::IStructuredDocumentTag::set_Title method
linktitle: set_Title
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::set_Title method. Specifies the friendly name associated with this SDT. Can not be null in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.markup/istructureddocumenttag/set_title/
---
## IStructuredDocumentTag::set_Title method


Specifies the friendly name associated with this SDT. Can not be null.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::set_Title(System::String value)
```

## Examples


Shows how to get structured document tag.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Structured document tags by id.docx"));

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
