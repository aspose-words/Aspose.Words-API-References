---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection-klass"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection-klass. En samling av IStructuredDocumentTag‑instanser som representerar de strukturerade dokumenttaggarna i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


En samling av [IStructuredDocumentTag](../istructureddocumenttag/)‑instanser som representerar de strukturerade dokumenttaggarna i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Count](./get_count/)() | Returnerar antalet strukturerade dokumenttaggar i samlingen. |
| [GetById](./getbyid/)(int32_t) | Returnerar den strukturerade dokumenttaggen med identifierare. |
| [GetByTag](./getbytag/)(const System::String\&) | Returnerar den första strukturerade dokumenttaggen som hittas i samlingen med den angivna taggen. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Returnerar den första strukturerade dokumenttaggen som hittas i samlingen med den angivna titeln. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar den strukturerade dokumenttaggen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Tar bort den strukturerade dokumenttaggen med den angivna identifieraren. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort en strukturerad dokumenttagg på det angivna indexet. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
