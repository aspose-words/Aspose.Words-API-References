---
title: "Aspose::Words::DocumentBase::get_Document metod"
linktitle: "get_Document"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase::get_Document metod. Hämtar den här instansen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Hämtar denna instans.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Exempel



Visar hur man skapar ett enkelt dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nya Document-objekt innehåller som standard den minsta uppsättningen av noder
// som krävs för att börja lägga till innehåll såsom text och former: en Section, en Body och ett Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Se även

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
