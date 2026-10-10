---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback interface"
linktitle: "IDocumentPartSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback interface. Implementera detta gränssnitt om du vill få meddelanden och kontrollera hur Aspose.Words sparar dokumentdelar när du exporterar ett dokument till Html- eller Epub-format i C++."
type: docs
weight: 40000
url: /sv/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Implementera detta gränssnitt om du vill få meddelanden och kontrollera hur Aspose.Words sparar dokumentdelar när du exporterar ett dokument till [Html](../../aspose.words/saveformat/) eller [Epub](../../aspose.words/saveformat/) format.

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Kallas när Aspose.Words håller på att spara en dokumentdel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
