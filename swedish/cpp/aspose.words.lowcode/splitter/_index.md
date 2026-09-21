---
title: "Aspose::Words::LowCode::Splitter klass"
linktitle: "Splitter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Splitter klass. Tillhandahåller metoder avsedda att dela upp dokumenten i delar med olika kriterier i C++."
type: docs
weight: 1500
url: /sv/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Tillhandahåller metoder avsedda för att dela upp dokumenten i delar med olika kriterier.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Skapar en ny instans av splitter‑processorn. |
| [Execute](../processor/execute/)() | Utför processorns åtgärd. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Utför processorns åtgärd som möjliggör avbrytning av dokumentbehandlingsuppgift med angivet avbokningstoken. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Extraherar ett specificerat sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil. Utdatafilens format bestäms av filnamnets filändelse. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extraherar ett specificerat sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extraherar ett specificerat sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extraherar ett specificerat sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extraherar ett specificerat sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet. |
| [From](../processor/from/)(const System::String\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Tar bort tomma sidor från dokumentet och sparar resultatet. Returnerar en lista med sidnummer som togs bort. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Tar bort tomma sidor från dokumentet och sparar resultatet i det specificerade formatet. Returnerar en lista med sidnummer som togs bort. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Tar bort tomma sidor från dokumentet och sparar resultatet i det specificerade formatet. Returnerar en lista med sidnummer som togs bort. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Tar bort blanka sidor från ett dokument som tillhandahålls i en inmatningsström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista med sidnummer som togs bort. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Tar bort blanka sidor från ett dokument som tillhandahålls i en inmatningsström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista med sidnummer som togs bort. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Delar ett dokument i flera delar baserat på de specificerade delningsalternativen och sparar de resulterande delarna till filer. Utdatafilens format bestäms av filnamnets filändelse. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Delar ett dokument i flera delar baserat på de specificerade delningsalternativen och sparar de resulterande delarna till filer i det angivna sparformatet. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Delar ett dokument i flera delar baserat på de specificerade delningsalternativen och sparar de resulterande delarna till filer i det angivna sparformatet. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Delar ett dokument från en inmatningsström i flera delar baserat på de specificerade delningsalternativen och returnerar de resulterande delarna som en array av strömmar i det angivna sparformatet. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Delar ett dokument från en inmatningsström i flera delar baserat på de specificerade delningsalternativen och returnerar de resulterande delarna som en array av strömmar i det angivna sparformatet. |
| [To](../processor/to/)(const System::String\&) | Anger utfil för processorn. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Anger utfil för processorn. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Anger utfil för processorn. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Anger utström för processorn. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Anger utström för processorn. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Se även

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
