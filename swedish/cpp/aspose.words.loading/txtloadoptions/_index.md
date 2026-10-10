---
title: "Aspose::Words::Loading::TxtLoadOptions klass"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtLoadOptions-klass. Gör det möjligt att ange ytterligare alternativ när ett Text‑dokument laddas in i ett Document‑objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


Gör det möjligt att ange ytterligare alternativ när ett [Text](../../aspose.words/loadformat/)‑dokument laddas in i ett [Document](../../aspose.words/document/)‑objekt. För att lära dig mer, besök dokumentationsartikeln [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Hämtar eller anger ett booleskt värde som indikerar om automatisk numreringsdetektering ska utföras vid inläsning av ett dokument. Standardvärdet är **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Hämtar eller anger strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er när det behövs. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Hämtar eller anger om metafil([Wmf](../) eller [Emf](../)) bilder ska konverteras till [Png](../) bildformat. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Hämtar eller anger om former med EquationXML ska konverteras till Office [Math](../../aspose.words.math/) objekt. |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Anger om hyperlänkar ska detekteras i text. Standardvärdet är **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Gör det möjligt att ange hur numrerade listobjekt identifieras när ett dokument importeras från vanligt textformat. Standardvärdet är **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Hämtar eller anger en dokumentriktning. Standardvärdet är [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara **null**. Standardvärdet är **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Tillåter att ange dokumentets teckensnittinställningar. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Anger om OLE-data ska ignoreras. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Hämtar eller anger föredragen alternativ för hantering av inledande mellanslag. Standardvärdet är [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Anger formatet för dokumentet som ska laddas. Standard är [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet är [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Hämtar eller anger lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Hämtar eller anger om INCLUDEPICTURE-fältet ska bevaras när Microsoft Word-format läses. Standardvärdet är **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definierar hur dokumentet ska hanteras om fel uppstår under laddning. Använd den här egenskapen för att ange om systemet ska försöka återställa dokumentet eller följa ett annat definierat beteende. Standardvärdet är [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Tillåter att använda temporära filer när dokument läses. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Hämtar eller anger föredragen alternativ för hantering av avslutande mellanslag. Standardvärdet är [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Anger om fält med **dirty**-attributet ska uppdateras. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Hämtar eller anger om LCID-värdet som hämtas från Windows-registret ska användas för att bestämma standards marginaler för sidinställning. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Sättare för [Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection](./get_autonumberingdetection/). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Sättare för [Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks](./get_detecthyperlinks/). |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Sättare för [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Sättare för [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Sättare för [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Sättare för [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Sättare för [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Sättare för [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Sättare för [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| [TxtLoadOptions](./txtloadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man läser och visar hyperlänkar.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Läs in dokument med hyperlänkar.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Skriv ut hyperlänkt text.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Se även

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
