---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById metod"
linktitle: "GetById"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById metod. Returnerar det strukturerade dokumenttagget efter identifierare i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Returnerar den strukturerade dokumenttaggen med identifierare.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| id | int32_t | Den strukturerade dokumenttaggens identifierare. |
## Anmärkningar


Returnerar null om det strukturerade dokumenttagget med den angivna identifieraren inte kan hittas.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
