---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title metod"
linktitle: "get_Title"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title method. Anger det vänliga namnet som är associerat med denna SDT. Kan inte vara null i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


Anger det vänliga namnet som är associerat med denna **SDT**. Kan inte vara null.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
```


## Exempel



Visar hur man hämtar en strukturerad dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Hämta den strukturerade dokumenttaggen efter Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Hämta den strukturerade dokumenttaggen eller ett intervalltagg efter titel.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Se även

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
