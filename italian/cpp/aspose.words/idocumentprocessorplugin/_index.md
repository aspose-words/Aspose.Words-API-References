---
title: "Interfaccia Aspose::Words::IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::IDocumentProcessorPlugin. Definisce un'interfaccia per plugin di elaborazione documenti esterni in C++."
type: docs
weight: 76750
url: /it/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Definisce un'interfaccia per plugin di elaborazione documento esterno.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Aggiungi il documento caricandolo con le opzioni di caricamento specificate. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Carica il documento usando le opzioni di caricamento specificate. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Salva il documento caricato dal metodo [Load()](./load/) nello stream di output usando le opzioni di salvataggio specificate. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Aggiunge un watermark immagine su ogni pagina del documento caricato dal metodo [Load()](./load/). |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Aggiunge un watermark testuale su ogni pagina del documento caricato dal metodo [Load()](./load/). |
| virtual [ToDocument](./todocument/)() | Analizza il documento caricato dal metodo [Load()](./load/) in un oggetto [Document](../document/). |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Salva ogni pagina del documento caricato dal metodo [Load()](./load/) usando le opzioni di salvataggio pagina fissa specificate. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
