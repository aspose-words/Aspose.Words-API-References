---
title: "Aspose::Words::LowCode::Converter-klass"
linktitle: "Converter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Converter-klass. Representerar en grupp metoder avsedda att konvertera en mängd olika dokumenttyper med en enda kodrad i C++."
type: docs
weight: 600
url: /sv/cpp/aspose.words.lowcode/converter/
---
## Converter class


Representerar en grupp av metoder avsedda för att konvertera en mängd olika dokumenttyper med en enda kodrad.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Konverterar det angivna indatadokumentet till utdata‑dokumentet med angivna in‑ och utfilnamn samt deras filändelser. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Konverterar det angivna indatadokumentet till utdata‑dokumentet med angivna in‑ och utfilnamn samt det slutgiltiga dokumentformatet. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konverterar det angivna indatadokumentet till utdata‑dokumentet med angivna in‑ och utfilnamn samt sparalternativ. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konverterar det angivna indatadokumentet till utdata‑dokumentet med angivna in‑ och utfilnamn samt dess ladd‑/sparalternativ. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Konverterar det angivna indatadokumentet till ett enda utdata‑dokument med angivna in‑ och ut‑strömmar. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konverterar det angivna indatadokumentet till ett enda utdata‑dokument med angivna in‑ och ut‑strömmar. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konverterar det angivna indatadokumentet till ett enda utdata‑dokument med angivna in‑ och ut‑strömmar. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Konverterar sidorna i den angivna indatafilen till bildfiler. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Konverterar sidorna i den angivna indatafilen till bildfiler i det angivna formatet. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konverterar sidorna i den angivna indatafilen till bildfiler med de angivna sparalternativen. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konverterar sidorna i den angivna indatafilen till bildfiler med de tillhandahållna ladd‑ och sparalternativen. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Konverterar sidorna i den angivna indatafilen till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konverterar sidorna i den angivna indatafilen till bilder med de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Konverterar sidorna i den angivna indata‑strömmen till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konverterar sidorna i den angivna indata‑strömmen till bilder med de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konverterar sidorna i den angivna indata‑strömmen till bilder med de tillhandahållna ladd‑ och sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Konverterar sidorna i det angivna dokumentet till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konverterar sidorna i det angivna dokumentet till bilder med de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [Create](./create/)() | Skapar en ny instans av konverteringsprocessorn. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Skapar en ny instans av konverteringsprocessorn. |
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
## Anmärkningar


De angivna in- och utdatafilerna eller strömmarna, tillsammans med det önskade sparformatet, används för att konvertera det givna indatadokumentet i ett format till utdata-dokumentet i det andra angivna formatet.

Konverteringsfunktionaliteten stöder över 35+ olika filformat.

Gruppen av metoder [ConvertToImages()](../) är utformad för att omvandla dokument till bilder, där varje sida konverteras till en separat bildfil. Dessa metoder konverterar också PDF‑dokument direkt till fast‑sidformat utan att ladda dem i dokumentmodellen, vilket förbättrar både prestanda och noggrannhet.

Med [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/) kan du ange en specifik uppsättning sidor som ska konverteras till bilder.
## Se även

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
