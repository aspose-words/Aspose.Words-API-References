---
title: "Aspose::Words::LowCode::Replacer klass"
linktitle: "Replacer"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Replacer klass. Tillhandahåller metoder avsedda att hitta och ersätta text i dokumentet i C++."
type: docs
weight: 1250
url: /sv/cpp/aspose.words.lowcode/replacer/
---
## Replacer class


Tillhandahåller metoder avsedda för att hitta och ersätta text i dokumentet.

```cpp
class Replacer : public Aspose::Words::LowCode::Processor
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ReplacerContext\>\&) | Skapar en ny instans av ersättningsprocessorn. |
| [Execute](../processor/execute/)() | Utför processorns åtgärd. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Utför processorns åtgärd som möjliggör avbrytning av dokumentbehandlingsuppgift med angivet avbokningstoken. |
| [From](../processor/from/)(const System::String\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Anger indatadokument för bearbetning. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Anger indatadokument för bearbetning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet teckensträngsmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet reguljärt uttrycksmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet reguljärt uttrycksmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett angivet reguljärt uttrycksmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett angivet reguljärt uttrycksmönster med en ersättningssträng i indatafilen. Renderar utdata till bilder. |
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
