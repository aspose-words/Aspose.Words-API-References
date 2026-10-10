---
title: "Interfaccia Aspose::Words::IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::IDocumentConverterPlugin. Definisce un'interfaccia per plugin di conversione esterni in C++."
type: docs
weight: 76250
url: /it/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Definisce un'interfaccia per plugin convertitore esterno.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Converte il documento utilizzando i flussi di input/output specificati e le opzioni di salvataggio. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Converte le pagine del documento dal flusso di input a un array di immagini. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
