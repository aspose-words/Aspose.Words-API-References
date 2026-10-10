---
title: "Aspose::Words::IDocumentProcessorPlugin Schnittstelle"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentProcessorPlugin Schnittstelle. Definiert eine Schnittstelle für ein externes Dokumentenverarbeitungs-Plugin in C++."
type: docs
weight: 76750
url: /de/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Definiert eine Schnittstelle für ein externes Dokumentverarbeitungs‑Plugin.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Fügen Sie das Dokument hinzu, indem Sie es mit den angegebenen Ladeoptionen laden. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Laden Sie das Dokument mit den angegebenen Ladeoptionen. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Speichern Sie das durch die Methode [Load()](./load/) geladene Dokument in den Ausgabestream unter Verwendung der angegebenen Speicheroptionen. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Fügt jeder Seite des durch die Methode [Load()](./load/) geladenen Dokuments ein Bildwasserzeichen hinzu. |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Fügt jeder Seite des durch die Methode [Load()](./load/) geladenen Dokuments ein Textwasserzeichen hinzu. |
| virtual [ToDocument](./todocument/)() | Parst das durch die Methode [Load()](./load/) geladene Dokument in ein [Document](../document/)-Objekt. |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Speichert jede Seite des durch die Methode [Load()](./load/) geladenen Dokuments unter Verwendung der angegebenen festen Seiten-Speicheroptionen. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
