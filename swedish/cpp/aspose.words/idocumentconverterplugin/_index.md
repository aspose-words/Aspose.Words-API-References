---
title: "Aspose::Words::IDocumentConverterPlugin-gränssnitt"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentConverterPlugin-gränssnitt. Definierar ett gränssnitt för extern konverteringsplugin i C++."
type: docs
weight: 76250
url: /sv/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Definierar ett gränssnitt för ett externt konverterings-plugin.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Konverterar dokument med angivna in- och utdataflöden samt sparalternativ. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Konverterar sidor från dokumentet från indataflöde till en matris av bilder. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
