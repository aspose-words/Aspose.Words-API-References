---
title: "Aspose::Words::IDocumentConverterPlugin Schnittstelle"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentConverterPlugin Schnittstelle. Definiert eine Schnittstelle für ein externes Konverter‑Plugin in C++."
type: docs
weight: 76250
url: /de/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Definiert eine Schnittstelle für ein externes Konverter-Plugin.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Konvertiert ein Dokument mithilfe der angegebenen Eingabe‑ und Ausgabeströme sowie Speicheroptionen. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Konvertiert Seiten aus einem Dokument vom Eingabestrom in ein Bildarray. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
