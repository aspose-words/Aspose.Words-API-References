---
title: "Aspose::Words::Saving::DocumentPartSavingArgs class"
linktitle: "DocumentPartSavingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocumentPartSavingArgs class. Tillhandahåller data för DocumentPartSaving()-återanropet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Tillhandahåller data för [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/) återanropet. För att lära dig mer, besök dokumentationsartikeln [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Document](./get_document/)() const | Hämtar dokumentobjektet som sparas. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Hämtar eller anger filnamnet (utan sökväg) där dokumentdelen ska sparas. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Tillåter att ange strömmen där dokumentdelen ska sparas. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en dokumentdel har sparats. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | Sättare för [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Inställare för [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Inställare för [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## Anmärkningar


När Aspose.Words sparar ett dokument till HTML eller relaterade format och [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/) är angivet, delas dokumentet upp i delar och som standard sparas varje dokumentdel i en separat fil.

Klassen [DocumentPartSavingArgs](./) låter dig kontrollera hur varje dokumentdel ska sparas. Den gör det möjligt att omdefiniera hur filnamn genereras eller att helt undvika sparande av dokumentdelar i filer genom att tillhandahålla egna strömobjekt.

För att spara dokumentdelar i strömmar istället för filer, använd egenskapen [DocumentPartStream](./get_documentpartstream/).
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
