---
title: "Aspose::Words::Saving::WordML2003SaveOptions‑klass"
linktitle: "WordML2003SaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::WordML2003SaveOptions‑klass. Kan användas för att ange ytterligare alternativ när ett dokument sparas i WordML‑formatet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words.saving/wordml2003saveoptions/
---
## WordML2003SaveOptions class


Kan användas för att ange ytterligare alternativ när ett dokument sparas i [WordML](../../aspose.words/saveformat/)-formatet. För att lära dig mer, besök dokumentationsartikeln [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class WordML2003SaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Skapar ett spara‑alternativ‑objekt av en klass som är lämplig för det angivna spara‑formatet. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Skapar ett sparaalternativobjekt av en klass som är lämplig för filändelsen som anges i det givna filnamnet. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Hämtar eller anger ett booleskt värde som indikerar om inbäddning av teckensnitt med PostScript‑konturer ska tillåtas när TrueType‑teckensnitt inbäddas i ett dokument när det sparas. Standardvärdet är **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Hämtar eller anger en anpassad lokal tidszon som används för datum/tids‑fält. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Hämtar eller anger sökvägen till standardmall (inklusive filnamn). Standardvärdet för denna egenskap är **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Hämtar ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Hämtar eller anger ett värde som bestämmer hur DrawingML‑effekter renderas. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur DrawingML‑former renderas. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | När **true** görs namn och version av Aspose.Words inbäddade i de skapade filerna. Standardvärdet är **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Hämtar värdet som bestämmer om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | När **true**, formaterar output snyggt där det är tillämpligt. Standardvärdet är **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Kallas under sparande av ett dokument och accepterar data om sparningsförloppet. |
| [get_SaveFormat](./get_saveformat/)() override | Anger det format som dokumentet kommer att sparas i om detta spara‑alternativ‑objekt används. Kan endast vara [WordML](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Anger mappen för temporära filer som används vid sparande till en DOC- eller DOCX-fil. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Bestämmer om teckensnittsattributen ska ändras enligt den teckenkod som används. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) uppdateras före sparande. Standardvärdet är **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Hämtar ett värde som bestämmer om fält av vissa typer ska uppdateras före sparande av dokumentet till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) uppdateras före sparande. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) uppdateras före sparande. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Hämtar ett värde som bestämmer om presentationsbilden för OLE-kontroller kommer att uppdateras. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Hämtar eller anger ett värde som bestämmer om anti-aliasing ska användas för rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Hämtar eller anger ett värde som bestämmer om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sättare för [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Ställer in ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Ställer in värdet som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Inställning för [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Sättare för [Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Anger ett värde som bestämmer om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Anger ett värde som bestämmer om presentationsbilden för OLE‑kontroller ska uppdateras. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |
## Anmärkningar


För närvarande tillhandahåller endast egenskapen [SaveFormat](./get_saveformat/), men i framtiden kan andra alternativ läggas till.

## Exempel



Visar hur man hanterar det råa innehållet i utmatningsdokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Skapa ett "WordML2003SaveOptions"‑objekt för att skicka till dokumentets "Save"‑metod
// för att ändra hur vi sparar dokumentet i WordML‑sparaformatet.
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::WordML, options->get_SaveFormat());

// Ställ in egenskapen "PrettyFormat" till "true" för att tillämpa tabbtecken‑indrag och
// radbrytningar för att göra det råa innehållet i utmatningsdokumentet lättare att läsa.
// Ställ in egenskapen "PrettyFormat" till "false" för att spara dokumentets råa innehåll i en kontinuerlig textmassa.
options->set_PrettyFormat(prettyFormat);

doc->Save(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml", options);

System::String fileContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml");
System::String newLine = System::Environment::get_NewLine();
if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(System::String::Format(u"<o:DocumentProperties>{0}\t\t", newLine) + System::String::Format(u"<o:Revision>1</o:Revision>{0}\t\t", newLine) + System::String::Format(u"<o:TotalTime>0</o:TotalTime>{0}\t\t", newLine) + System::String::Format(u"<o:Pages>1</o:Pages>{0}\t\t", newLine) + System::String::Format(u"<o:Words>0</o:Words>{0}\t\t", newLine) + System::String::Format(u"<o:Characters>0</o:Characters>{0}\t\t", newLine) + System::String::Format(u"<o:Lines>1</o:Lines>{0}\t\t", newLine) + System::String::Format(u"<o:Paragraphs>1</o:Paragraphs>{0}\t\t", newLine) + System::String::Format(u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{0}\t\t", newLine) + System::String::Format(u"<o:Version>11.5606</o:Version>{0}\t", newLine) + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(System::String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") + u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```


Visar hur man hanterar minnesoptimering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Skapa ett "WordML2003SaveOptions"‑objekt för att skicka till dokumentets "Save"‑metod
// för att ändra hur vi sparar dokumentet i WordML‑sparaformatet.
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

// Ställ in flaggan "MemoryOptimization" till "true" för att minska minnesförbrukningen
// under dokumentets sparoperation på bekostnad av längre sparningstid.
// Ställ in flaggan "MemoryOptimization" till "false" för att spara dokumentet normalt.
options->set_MemoryOptimization(memoryOptimization);

doc->Save(get_ArtifactsDir() + u"WordML2003SaveOptions.MemoryOptimization.xml", options);
```

## Se även

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
