---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions class. Tillåter att ange ytterligare alternativ när ett HTML‑dokument laddas in i ett Document‑objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


Tillåter att ange ytterligare alternativ när ett HTML‑dokument laddas in i ett [Document](../../aspose.words/document/)‑objekt. För att lära dig mer, besök dokumentationsartikeln [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Hämtar eller anger strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er när det behövs. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Hämtar eller anger ett värde som specificerar hur egenskaper för blocknivåelement importeras. Standardvärdet är [Merge](../blockimportmode/). |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Hämtar eller anger om metafil([Wmf](../) eller [Emf](../)) bilder ska konverteras till [Png](../) bildformat. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Hämtar eller anger om former med EquationXML ska konverteras till Office [Math](../../aspose.words.math/) objekt. |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Hämtar eller anger ett värde som indikerar om inlästa SVG-bilder ska konverteras till EMF-format. Standardvärdet är **false** och, om möjligt, lagras inlästa SVG-bilder som de är utan konvertering. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara **null**. Standardvärdet är **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Tillåter att ange dokumentets teckensnittinställningar. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | Hämtar eller anger ett värde som indikerar om <noscript>-HTML-element ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Anger om OLE-data ska ignoreras. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Anger formatet för dokumentet som ska laddas. Standard är [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet är [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Hämtar eller anger lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | Hämtar eller anger föredragen typ av dokumentnoder som ska representera importerade <input>- och <select>-element. Standardvärdet är [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Hämtar eller anger om INCLUDEPICTURE-fältet ska bevaras när Microsoft Word-format läses. Standardvärdet är **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definierar hur dokumentet ska hanteras om fel uppstår under laddning. Använd den här egenskapen för att ange om systemet ska försöka återställa dokumentet eller följa ett annat definierat beteende. Standardvärdet är [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | Hämtar eller anger ett värde som indikerar om @font-face-regler ska stödjas och om deklarerade teckensnitt ska laddas. Standardvärdet är **false**. |
| [get_SupportVml](./get_supportvml/)() const | Hämtar eller anger ett värde som indikerar om VML-bilder ska stödjas. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Tillåter att använda temporära filer när dokument läses. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Anger om fält med **dirty**-attributet ska uppdateras. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Hämtar eller anger om LCID-värdet som hämtas från Windows-registret ska användas för att bestämma standards marginaler för sidinställning. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | Antalet millisekunder att vänta innan webbförfrågan tidsöverskrider. Standardvärdet är 100000 millisekunder (100 sekunder). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | Sättare för [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Sättare för [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Sättare för [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Sättare för [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Sättare för [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Sättare för [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Sättare för [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Sättare för [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | Sättare för [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | Antalet millisekunder att vänta innan webbförfrågan tidsöverskrider. Standardvärdet är 100000 millisekunder (100 sekunder). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man stödjer villkorliga kommentarer vid inläsning av ett HTML-dokument.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Om värdet är sant, tar vi VML-kod i beaktande när vi parsar det laddade dokumentet.
loadOptions->set_SupportVml(supportVml);

// Detta dokument innehåller en JPEG-bild inom "<!--[if gte vml 1]>"-taggar,
// och en annan PNG-bild inom "<![if !vml]>"-taggar.
// Om vi sätter flaggan "SupportVml" till "true" kommer Aspose.Words att ladda JPEG-filen.
// Om vi sätter denna flagga till "false" kommer Aspose.Words endast att ladda PNG-filen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Se även

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
