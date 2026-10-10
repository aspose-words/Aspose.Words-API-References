---
title: "Aspose::Words::LowCode::Comparer class"
linktitle: "Comparer"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Comparer class. Tillhandahåller metoder avsedda för att jämföra dokument i C++."
type: docs
weight: 500
url: /sv/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Tillhandahåller metoder avsedda för att jämföra dokument.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument som lästs in från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det specificerade sparformatet, vilket skapar förändringar som ett antal redigerings- och formatrevisioner. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Jämför två dokument och sparar skillnaderna som bilder. Varje objekt i den returnerade arrayen representerar en enskild sida av utdata renderad som en bild. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument och sparar skillnaderna som bilder. Varje objekt i den returnerade arrayen representerar en enskild sida av utdata renderad som en bild. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Jämför två dokument och sparar skillnaderna som bilder. Varje objekt i den returnerade arrayen representerar en enskild sida av utdata renderad som en bild. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför två dokument och sparar skillnaderna som bilder. Varje objekt i den returnerade arrayen representerar en enskild sida av utdata renderad som en bild. |
| static [Create](./create/)() | Skapar en ny instans av konverteringsprocessorn. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Skapar en ny instans av jämförelseprocessorn. |
| [Execute](../processor/execute/)() | Utför processorns åtgärd. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Utför processorns åtgärd som möjliggör avbrytning av dokumentbehandlingsuppgift med angivet avbokningstoken. |
| [From](../processor/from/)(const System::String\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
