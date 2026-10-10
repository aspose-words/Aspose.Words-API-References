---
title: "Aspose::Words::LowCode::Merger klass"
linktitle: "Merger"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Merger klass. Representerar en grupp metoder avsedda att slå samman en mängd olika typer av dokument till ett enda utdata-dokument i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lowcode/merger/
---
## Merger class


Representerar en grupp av metoder avsedda för att slå samman en mängd olika dokumenttyper till ett enda utdata‑dokument.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Create](./create/)() | Skapar en ny instans av e-postsammanfogningsprocessorn. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Skapar en ny instans av e-postsammanfogningsprocessorn. |
| [Execute](../processor/execute/)() | Utför processorns åtgärd. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Utför processorns åtgärd som möjliggör avbrytning av dokumentbehandlingsuppgift med angivet avbokningstoken. |
| [From](../processor/from/)(const System::String\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utfilnamn med hjälp av [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utfilnamn och det slutgiltiga dokumentformatet. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utfilnamn samt sparalternativ. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utfilnamn samt sparalternativ. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda dokument och returnerar en [Document](../../aspose.words/document/) instans av det slutgiltiga dokumentet. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda dokument och returnerar en [Document](../../aspose.words/document/) instans av det slutgiltiga dokumentet. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda dokument och returnerar en [Document](../../aspose.words/document/) instans av det slutgiltiga dokumentet. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utströmar och det slutgiltiga dokumentformatet. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utströmar samt sparalternativ. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utströmar samt sparalternativ. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda dokument och returnerar en [Document](../../aspose.words/document/) instans av det slutgiltiga dokumentet. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda dokument och returnerar en [Document](../../aspose.words/document/) instans av det slutgiltiga dokumentet. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utfilnamn samt sparalternativ. Renderar utdata till bilder. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Slår samman de angivna indatadokumentströmarna till ett enda utdata-dokument med angivna bildsparalternativ. Renderar utdata till bilder. |
| [To](../processor/to/)(const System::String\&) | Anger utfil för processorn. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Anger utfil för processorn. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Anger utfil för processorn. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Anger utström för processorn. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Anger utström för processorn. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Anmärkningar


De angivna in- och utfilernas eller strömmarnas, tillsammans med önskade sammanslagnings- och sparalternativ, används för att slå samman de angivna indatadokumenten till ett enda utdata-dokument.

Sammanslagningsfunktionen stöder över 35 olika filformat.
## Se även

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
