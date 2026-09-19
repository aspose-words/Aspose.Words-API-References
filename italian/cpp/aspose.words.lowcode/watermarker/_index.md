---
title: "Aspose::Words::LowCode::Watermarker class"
linktitle: "Watermarker"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::Watermarker. Fornisce metodi destinati a inserire filigrane nei documenti in C++."
type: docs
weight: 1750
url: /it/cpp/aspose.words.lowcode/watermarker/
---
## Watermarker class


Fornisce metodi destinati a inserire filigrane nei documenti.

```cpp
class Watermarker : public Aspose::Words::LowCode::Processor
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::WatermarkerContext\>\&) | Crea una nuova istanza del processore di filigrane. |
| [Execute](../processor/execute/)() | Esegui l'azione del processore. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Esegui l'azione del processore consentendo l'annullamento dell'attività di elaborazione del documento utilizzando il token di cancellazione specificato. |
| [From](../processor/from/)(const System::String\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&) | Aggiunge una filigrana immagine al documento. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento con opzioni. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento con opzioni e formato di salvataggio specificato. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento da flussi con opzioni. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&) | Aggiunge una filigrana di testo al documento. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento con opzioni. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) | Aggiunge una filigrana di testo al documento da flussi con opzioni. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento da flussi con opzioni. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Aggiunge una filigrana di testo al documento da flussi con opzioni. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento da flussi con opzioni. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Aggiunge una filigrana di testo al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Aggiunge una filigrana di testo al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) | Aggiunge una filigrana immagine al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Aggiunge una filigrana immagine al documento con opzioni. Renderizza l'output in immagini. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento con opzioni. Renderizza l'output in immagini. |
| [To](../processor/to/)(const System::String\&) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifica il flusso di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifica il flusso di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Vedi anche

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
