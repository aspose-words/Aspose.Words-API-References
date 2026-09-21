---
title: "Aspose::Words::FileFormatUtil klass"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatUtil klass. Tillhandahåller verktygsmetoder för att arbeta med filformat, såsom att upptäcka filformat eller konvertera filändelser till/från filformat‑enumerationer. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Tillhandahåller hjälpfunktioner för att arbeta med filformat, såsom att upptäcka filformat eller konvertera filändelser till/från filformatenumerationer. För att läsa mer, besök artikeln [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) i dokumentationen.

```cpp
class FileFormatUtil
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Konverterar IANA‑innehållstyp till ett laddningsformat‑enumerationsvärde. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Konverterar IANA‑innehållstyp till ett sparformat‑enumerationsvärde. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Detekterar och returnerar information om formatet för ett dokument som lagras i en diskfil. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Detekterar och returnerar information om formatet för ett dokument som lagras i en ström. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Konverterar en filnamnsändelse till ett [SaveFormat](../saveformat/)‑värde. |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Konverterar ett Aspose.Words‑bildtyp‑enumerationsvärde till en filändelse. Den returnerade ändelsen är en gemener‑sträng med en inledande punkt. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Konverterar ett laddningsformat‑enumerationsvärde till en filändelse. Den returnerade ändelsen är en gemener‑sträng med en inledande punkt. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Konverterar ett [LoadFormat](../loadformat/)‑värde till ett [SaveFormat](../saveformat/)‑värde om möjligt. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Konverterar ett enumererat värde för sparaformat till en filändelse. Den returnerade ändelsen är en gemener sträng med en inledande punkt. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Konverterar ett [SaveFormat](../saveformat/)‑värde till ett [LoadFormat](../loadformat/)‑värde om möjligt. |

## Exempel



Visar hur man upptäcker kodning i en html‑fil.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Egenskapen Encoding används endast när vi skapar ett FileFormatInfo‑objekt för ett html‑dokument.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
