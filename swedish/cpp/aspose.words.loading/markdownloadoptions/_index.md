---
title: "Aspose::Words::Loading::MarkdownLoadOptions klass"
linktitle: "MarkdownLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::MarkdownLoadOptions klass. Tillåter att ange ytterligare alternativ när du laddar ett Markdown-dokument till ett Document-objekt i C++."
type: docs
weight: 5500
url: /sv/cpp/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class


Tillåter att ange ytterligare alternativ när du laddar ett [Markdown](../../aspose.words/loadformat/) dokument till ett [Document](../../aspose.words/document/) objekt.

```cpp
class MarkdownLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Hämtar eller anger strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er när det behövs. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Hämtar eller anger om metafil([Wmf](../) eller [Emf](../)) bilder ska konverteras till [Png](../) bildformat. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Hämtar eller anger om former med EquationXML ska konverteras till Office [Math](../../aspose.words.math/) objekt. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara **null**. Standardvärdet är **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Tillåter att ange dokumentets teckensnittinställningar. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Anger om OLE-data ska ignoreras. |
| [get_ImportUnderlineFormatting](./get_importunderlineformatting/)() const | Hämtar eller anger ett booleskt värde som indikerar om en sekvens av två plustecken "++" ska kännas som understruken textformatering. Standardvärdet är **false**. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Anger formatet för dokumentet som ska laddas. Standard är [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet är [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Hämtar eller anger lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_PreserveEmptyLines](./get_preserveemptylines/)() const | Hämtar eller anger ett booleskt värde som indikerar om tomma rader ska bevaras när ett [Markdown](../../aspose.words/loadformat/) dokument laddas. Standardvärdet är **false**. Vanligtvis ignoreras tomma rader mellan blocknivåelement i Markdown. Tomma rader i början och slutet av dokumentet ignoreras också. Detta alternativ tillåter att importera sådana tomma rader. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Hämtar eller anger om INCLUDEPICTURE-fältet ska bevaras när Microsoft Word-format läses. Standardvärdet är **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definierar hur dokumentet ska hanteras om fel uppstår under laddning. Använd den här egenskapen för att ange om systemet ska försöka återställa dokumentet eller följa ett annat definierat beteende. Standardvärdet är [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [get_SoftLineBreakCharacter](./get_softlinebreakcharacter/)() const | Hämtar eller anger ett teckenvärde som representerar **soft line break**. Standardvärdet är **SPACE (U+0020)**. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Tillåter att använda temporära filer när dokument läses. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Anger om fält med **dirty**-attributet ska uppdateras. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Hämtar eller anger om LCID-värdet som hämtas från Windows-registret ska användas för att bestämma standards marginaler för sidinställning. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena. |
| [MarkdownLoadOptions](./markdownloadoptions/)() | Initierar en ny instans av klassen [MarkdownLoadOptions](./). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_ImportUnderlineFormatting](./set_importunderlineformatting/)(bool) | Sättare för [Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting](./get_importunderlineformatting/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Sättare för [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Sättare för [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveEmptyLines](./set_preserveemptylines/)(bool) | Sättare för [Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines](./get_preserveemptylines/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Sättare för [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [set_SoftLineBreakCharacter](./set_softlinebreakcharacter/)(char16_t) | Sättare för [Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter](./get_softlinebreakcharacter/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man bevarar tomma rader när ett dokument laddas.
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## Se även

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
