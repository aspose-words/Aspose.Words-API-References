---
title: "Aspose::Words::Loading::LoadOptions-klass"
linktitle: "LoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions-klass. Tillåter att ange ytterligare alternativ (såsom lösenord eller bas-URI) när ett dokument laddas in i ett Document-objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Tillåter att ange ytterligare alternativ (såsom lösenord eller bas-URI) när ett dokument laddas in i ett [Document](../../aspose.words/document/) objekt. För att lära dig mer, besök [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) dokumentationsartikel.

```cpp
class LoadOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_BaseUri](./get_baseuri/)() const | Hämtar eller anger strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er när det behövs. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Hämtar eller anger om metafil([Wmf](../) eller [Emf](../)) bilder ska konverteras till [Png](../) bildformat. |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | Hämtar eller anger om former med EquationXML ska konverteras till Office [Math](../../aspose.words.math/) objekt. |
| [get_Encoding](./get_encoding/)() const | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara **null**. Standardvärdet är **null**. |
| [get_FontSettings](./get_fontsettings/)() const | Tillåter att ange dokumentets teckensnittinställningar. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | Anger om OLE-data ska ignoreras. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [get_LoadFormat](./get_loadformat/)() const | Anger formatet för dokumentet som ska laddas. Standard är [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet är [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | Hämtar eller anger lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. Standardvärdet är **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Hämtar eller anger om INCLUDEPICTURE-fältet ska bevaras när Microsoft Word-format läses. Standardvärdet är **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [get_RecoveryMode](./get_recoverymode/)() const | Definierar hur dokumentet ska hanteras om fel uppstår under laddning. Använd den här egenskapen för att ange om systemet ska försöka återställa dokumentet eller följa ett annat definierat beteende. Standardvärdet är [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [get_TempFolder](./get_tempfolder/)() const | Tillåter att använda temporära filer när dokument läses. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | Anger om fält med **dirty**-attributet ska uppdateras. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | Hämtar eller anger om LCID-värdet som hämtas från Windows-registret ska användas för att bestämma standards marginaler för sidinställning. |
| [get_WarningCallback](./get_warningcallback/)() const | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |
| [LoadOptions](./loadoptions/)(const System::String\&) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | Inställare för [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/). |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | Inställare för [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | Inställare för [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Inställare för [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/). |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/). |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | Sättare för [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Sättare för [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/). |
| [set_Password](./set_password/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/). |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Kallas under laddning av ett dokument och tar emot data om laddningsförloppet. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Sättare för [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/). |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Tillåter att kontrollera hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Sättare för [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | Sättare för [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under en laddningsoperation när ett problem upptäcks som kan leda till förlust av data- eller formateringsnoggrannhet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man laddar ett krypterat Microsoft Word-dokument.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words kastar ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// När ett sådant dokument laddas, skickas lösenordet till dokumentets konstruktor med ett LoadOptions-objekt.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Det finns två sätt att ladda ett krypterat dokument med ett LoadOptions-objekt.
// 1 -  Ladda dokumentet från det lokala filsystemet med filnamn:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Ladda dokumentet från en ström:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
