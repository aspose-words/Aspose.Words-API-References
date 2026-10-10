---
title: "Aspose::Words::Saving::MarkdownSaveOptions klass"
linktitle: "MarkdownSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions klass. Klass för att ange ytterligare alternativ när ett dokument sparas i Markdown-formatet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class


Klass för att ange ytterligare alternativ när ett dokument sparas i [Markdown](../../aspose.words/saveformat/) formatet. För att lära dig mer, besök dokumentationsartikeln [Ange sparalternativ](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class MarkdownSaveOptions : public Aspose::Words::Saving::TxtSaveOptionsBase
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
| [get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/)() const | Anger hur tomma stycken ska exporteras till Markdown. Standardvärdet är [EmptyLine](../markdownemptyparagraphexportmode/). |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | Anger kodningen som ska användas vid export i textformat. Standardvärdet är **Encoding.UTF8**. |
| [get_ExportAsHtml](./get_exportashtml/)() const | Tillåter att ange vilka element som ska exporteras till Markdown som rå HTML. Standardvärdet är [None](../markdownexportashtml/). |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | När **true** görs namn och version av Aspose.Words inbäddade i de skapade filerna. Standardvärdet är **true**. |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | Anger hur sidhuvuden och sidfötter exporteras till textformaten. Standardvärdet är [PrimaryOnly](../txtexportheadersfootersmode/). |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Anger om bilder sparas i Base64-format till utdatafilen. Standardvärdet är **false**. |
| [get_ExportUnderlineFormatting](./get_exportunderlineformatting/)() const | Hämtar eller anger ett booleskt värde som indikerar om understruken textformatering ska exporteras som en sekvens av två plustecken "++". Standardvärdet är **false**. |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | Tillåter att ange om sidbrytningar ska bevaras under export. Standardvärdet är **false**. |
| [get_ImageResolution](./get_imageresolution/)() const | Anger utskriftsupplösningen för bilder vid export till Markdown. Standard är **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Tillåter att styra hur bilder sparas när ett dokument sparas i [Markdown](../../aspose.words/saveformat/) format. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Anger den fysiska mappen där bilder sparas när ett dokument exporteras till [Markdown](../../aspose.words/saveformat/) formatet. Standard är en tom sträng. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett dokument. Standard är en tom sträng. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas. |
| [get_LinkExportMode](./get_linkexportmode/)() const | Anger hur länkar kommer att skrivas till utdatafilen. Standardvärdet är [Auto](../markdownlinkexportmode/). |
| [get_ListExportMode](./get_listexportmode/)() const | Anger hur listobjekt kommer att skrivas till utdatafilen. Standardvärdet är [MarkdownSyntax](../markdownlistexportmode/). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Hämtar värdet som bestämmer om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | Anger hur OfficeMath kommer att skrivas till utdatafilen. Standardvärdet är [Text](../markdownofficemathexportmode/). |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | Anger strängen som ska användas som styckebrytning vid export i textformat. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | När **true**, formaterar output snyggt där det är tillämpligt. Standardvärdet är **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Kallas under sparande av ett dokument och accepterar data om sparningsförloppet. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Tillåter att styra hur resurser sparas när ett dokument exporteras till [Markdown](../../aspose.words/saveformat/) format. |
| [get_SaveFormat](./get_saveformat/)() override | Anger det format som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endast vara [Markdown](../../aspose.words/saveformat/). |
| [get_TableContentAlignment](./get_tablecontentalignment/)() const | Hämtar eller anger ett värde som specificerar hur innehåll i tabeller ska justeras vid export till [Markdown](../../aspose.words/saveformat/) formatet. Standardvärdet är [Auto](../tablecontentalignment/). |
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
| [MarkdownSaveOptions](./markdownsaveoptions/)() | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument i [Markdown](../../aspose.words/saveformat/) formatet. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sättare för [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Ställer in ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_EmptyParagraphExportMode](./set_emptyparagraphexportmode/)(Aspose::Words::Saving::MarkdownEmptyParagraphExportMode) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/). |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Sättare för [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](../txtsaveoptionsbase/get_encoding/). |
| [set_ExportAsHtml](./set_exportashtml/)(Aspose::Words::Saving::MarkdownExportAsHtml) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml](./get_exportashtml/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | Sättare för [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportUnderlineFormatting](./set_exportunderlineformatting/)(bool) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting](./get_exportunderlineformatting/). |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | Sättare för [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Tillåter att styra hur bilder sparas när ett dokument sparas i [Markdown](../../aspose.words/saveformat/) format. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_LinkExportMode](./set_linkexportmode/)(Aspose::Words::Saving::MarkdownLinkExportMode) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode](./get_linkexportmode/). |
| [set_ListExportMode](./set_listexportmode/)(Aspose::Words::Saving::MarkdownListExportMode) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode](./get_listexportmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Ställer in värdet som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::MarkdownOfficeMathExportMode) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode](./get_officemathexportmode/). |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String\&) | Sättare för [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Inställning för [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Tillåter att styra hur resurser sparas när ett dokument exporteras till [Markdown](../../aspose.words/saveformat/) format. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Anger det format som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endast vara [Markdown](../../aspose.words/saveformat/). |
| [set_TableContentAlignment](./set_tablecontentalignment/)(Aspose::Words::Saving::TableContentAlignment) | Sättare för [Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment](./get_tablecontentalignment/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Anger ett värde som bestämmer om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Anger ett värde som bestämmer om presentationsbilden för OLE‑kontroller ska uppdateras. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |
## Se även

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
