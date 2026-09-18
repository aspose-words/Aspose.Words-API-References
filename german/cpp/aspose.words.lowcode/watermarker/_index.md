---
title: "Aspose::Words::LowCode::Watermarker class"
linktitle: "Watermarker"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Watermarker class. Stellt Methoden bereit, die zum Einfügen von Wasserzeichen in die Dokumente in C++ vorgesehen sind."
type: docs
weight: 1750
url: /de/cpp/aspose.words.lowcode/watermarker/
---
## Watermarker class


Stellt Methoden bereit, die zum Einfügen von Wasserzeichen in die Dokumente vorgesehen sind.

```cpp
class Watermarker : public Aspose::Words::LowCode::Processor
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::WatermarkerContext\>\&) | Erstellt eine neue Instanz des Watermarker‑Prozessors. |
| [Execute](../processor/execute/)() | Führt die Prozessoraktion aus. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Führt die Prozessoraktion aus und ermöglicht das Abbrechen des Dokumentverarbeitungsvorgangs mithilfe des angegebenen Abbruchtokens. |
| [From](../processor/from/)(const System::String\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&) | Fügt dem Dokument ein Bildwasserzeichen hinzu. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen hinzu. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen hinzu. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen und angegebenem Speicherformat hinzu. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen aus Streams mit Optionen hinzu. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt dem Dokument ein Textwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt dem Dokument ein Bildwasserzeichen mit Optionen hinzu. Rendert die Ausgabe als Bilder. |
| [To](../processor/to/)(const System::String\&) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Siehe auch

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
