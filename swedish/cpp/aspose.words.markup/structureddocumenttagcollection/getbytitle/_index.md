---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle metod"
linktitle: "GetByTitle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle metod. Returnerar det första strukturerade dokumenttagget som påträffas i samlingen med den angivna titeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Returnerar den första strukturerade dokumenttaggen som hittas i samlingen med den angivna titeln.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| titel | const System::String\& | Titeln på det strukturerade dokumenttagget. |
## Anmärkningar


Returnerar null om det strukturerade dokumenttagget med den angivna titeln inte kan hittas.

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
