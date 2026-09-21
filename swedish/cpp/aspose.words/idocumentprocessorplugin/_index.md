---
title: "Aspose::Words::IDocumentProcessorPlugin gränssnitt"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentProcessorPlugin gränssnitt. Definierar ett gränssnitt för extern dokumentprocessor-plugin i C++."
type: docs
weight: 76750
url: /sv/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Definierar ett gränssnitt för ett externt dokumentprocessor-plugin.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Lägg till dokumentet genom att ladda det med de angivna inläsningsalternativen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Läs in dokumentet med de angivna inläsningsalternativen. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Spara dokumentet som laddats av metoden [Load()](./load/) till utdataflödet med de angivna sparalternativen. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Lägger till bildvattenstämpel på varje sida i dokumentet som laddats av metoden [Load()](./load/). |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Lägger till textvattenstämpel på varje sida i dokumentet som laddats av metoden [Load()](./load/). |
| virtual [ToDocument](./todocument/)() | Analyserar dokumentet som laddats av metoden [Load()](./load/) till ett [Document](../document/)-objekt. |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Sparar varje sida i dokumentet som laddats av metoden [Load()](./load/) med de angivna fasta sid‑sparalternativen. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
