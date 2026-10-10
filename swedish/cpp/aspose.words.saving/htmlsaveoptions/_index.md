---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions class. Kan användas för att ange ytterligare alternativ när ett dokument sparas i Html-, Mhtml-, Epub-, Azw3- eller Mobi-format. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Kan användas för att ange ytterligare alternativ när ett dokument sparas i formatet [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) eller [Mobi](../../aspose.words/saveformat/). För att lära dig mer, besök dokumentationsartikeln [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Skapar ett spara‑alternativ‑objekt av en klass som är lämplig för det angivna spara‑formatet. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Skapar ett sparaalternativobjekt av en klass som är lämplig för filändelsen som anges i det givna filnamnet. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Hämtar eller anger ett booleskt värde som indikerar om inbäddning av teckensnitt med PostScript‑konturer ska tillåtas när TrueType‑teckensnitt inbäddas i ett dokument när det sparas. Standardvärdet är **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Anger om negativa vänstra och högra indrag i stycken normaliseras vid sparande till HTML, MHTML eller EPUB. Standardvärdet är **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Anger ett prefix som läggs till alla CSS‑klassnamn. Standardvärdet är en tom sträng och genererade CSS‑klassnamn har inget gemensamt prefix. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Gör det möjligt att styra hur CSS‑stilar sparas när ett dokument sparas till HTML, MHTML eller EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Anger sökvägen och namnet på Cascading [Style](../../aspose.words/style/) Sheet‑filen (CSS) som skrivs när ett dokument exporteras till HTML. Standard är en tom sträng. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Anger hur CSS (Cascading [Style](../../aspose.words/style/) Sheet)‑stilar exporteras till HTML, MHTML eller EPUB. Standardvärdet är [Inline](../cssstylesheettype/) för HTML/MHTML och [External](../cssstylesheettype/) för EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Hämtar eller anger en anpassad lokal tidszon som används för datum/tids‑fält. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Hämtar eller anger sökvägen till standardmall (inklusive filnamn). Standardvärdet för denna egenskap är **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Hämtar ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Hämtar eller anger ett värde som bestämmer hur DrawingML‑effekter renderas. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur DrawingML‑former renderas. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Gör det möjligt att styra hur dokumentdelar sparas när ett dokument sparas till HTML eller EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Anger hur dokumentet ska delas upp vid sparande till formatet [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) eller [Azw3](../../aspose.words/saveformat/). Standard är [None](../documentsplitcriteria/) för HTML och [HeadingParagraph](../documentsplitcriteria/) för EPUB och AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Anger den maximala rubriknivån där dokumentet ska delas upp. Standardvärdet är **%2**. |
| [get_Encoding](./get_encoding/)() const | Anger den kodning som ska användas vid export till HTML, MHTML eller EPUB. Standardvärdet är **new UTF8Encoding(false)** (UTF-8 utan BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Anger om CID (Content-ID)-URL:er ska användas för att referera resurser (bilder, teckensnitt, CSS) som ingår i MHTML‑dokument. Standardvärdet är **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Anger om inbyggda och anpassade dokumentegenskaper ska exporteras till HTML, MHTML eller EPUB. Standardvärdet är **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Styr hur rullgardinsformulärfält sparas till HTML eller MHTML. Standardvärdet är **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Anger om teckensnittresurser ska exporteras till HTML, MHTML eller EPUB. Standard är **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Anger om teckensnittresurser ska bäddas in i HTML med Base64‑kodning. Standard är **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | När **true** görs namn och version av Aspose.Words inbäddade i de skapade filerna. Standardvärdet är **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Anger hur sidhuvuden och sidfötter exporteras till HTML, MHTML eller EPUB. Standardvärdet är [PerSection](../exportheadersfootersmode/) för HTML/MHTML och [None](../exportheadersfootersmode/) för EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Anger om bilder sparas i Base64‑format i den utgående HTML, MHTML eller EPUB. Standard är **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Anger om språkinformation exporteras till HTML, MHTML eller EPUB. Standard är **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Styr hur listetiketter skrivs ut till HTML, MHTML eller EPUB. Standardvärdet är [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Anger om den ursprungliga URL:en ska användas som URL för de länkade bilderna. Standardvärdet är **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Anger om sidomarginaler exporteras till HTML, MHTML eller EPUB. Standard är **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Anger om sidinställningar exporteras till HTML, MHTML eller EPUB. Standard är **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Anger om teckenstorlekar ska skrivas ut i relativa enheter när man sparar till HTML, MHTML eller EPUB. Standard är **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Anger om rundresinformation ska skrivas när man sparar till HTML, MHTML eller EPUB. Standardvärdet är **true** för HTML och **false** för MHTML och EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Styr om [Shape](../../aspose.words.drawing/shape/)‑noder konverteras till SVG‑bilder när man sparar till HTML, MHTML, EPUB eller AZW3. Standardvärdet är **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Styr hur textinmatningsformulärfält sparas till HTML eller MHTML. Standardvärdet är **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Anger om sidnummer ska skrivas till innehållsförteckning när man sparar HTML, MHTML och EPUB. Standardvärdet är **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Anger om DOCTYPE‑deklarationen ska skrivas när man sparar till HTML eller MHTML. När **true** skrivs en DOCTYPE‑deklaration i dokumentet före rot‑elementet. Standardvärdet är **false**. Vid sparande till EPUB eller HTML5 ([Html5](../htmlversion/)) skrivs DOCTYPE‑deklarationen alltid. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Styr vilka teckensnittresurser som behöver delmängdsgenerering när man sparar till HTML, MHTML eller EPUB. Standard är **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Gör det möjligt att styra hur teckensnitt sparas när ett dokument sparas till HTML, MHTML eller EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Anger den fysiska mappen där teckensnitt sparas när ett dokument exporteras till HTML. Standard är en tom sträng. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Anger namnet på mappen som används för att konstruera teckensnitt-URI:er som skrivs in i ett HTML‑dokument. Standard är en tom sträng. |
| [get_HtmlVersion](./get_htmlversion/)() const | Anger version av HTML‑standarden som ska användas när dokumentet sparas till HTML eller MHTML. Standardvärdet är [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Anger utskriftsupplösningen för bilder när man exporterar till HTML, MHTML eller EPUB. Standard är **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Gör det möjligt att styra hur bilder sparas när ett dokument sparas till HTML, MHTML eller EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Anger den fysiska mappen där bilder sparas när ett dokument exporteras till HTML‑format. Standard är en tom sträng. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Anger namnet på mappen som används för att konstruera bild‑URI:er som skrivs in i ett HTML‑dokument. Standard är en tom sträng. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Hämtar värdet som bestämmer om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Anger i vilket format metafiler sparas när man exporterar till HTML, MHTML eller EPUB. Standardvärdet är [Png](../htmlmetafileformat/), vilket betyder att metafiler renderas till raster‑PNG‑bilder. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Anger den maximala nivån av rubriker som fylls i navigeringskartan när man exporterar till EPUB-, MOBI- eller AZW3‑format. Standardvärdet är **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Styr hur OfficeMath‑objekt exporteras till HTML, MHTML eller EPUB. Standardvärdet är [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | När **true**, formaterar output snyggt där det är tillämpligt. Standardvärdet är **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Kallas under sparande av ett dokument och accepterar data om sparningsförloppet. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Anger om JavaScript kommer att tas bort från länkar. Standard är **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Anger om bakstrecks-tecken ska ersättas med yen-tecken. Standardvärdet är **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Anger om teckensnittsfamiljenamn som används i dokumentet ska lösas upp och ersättas enligt [FontSettings](../../aspose.words/document/get_fontsettings/) när de skrivs till HTML-baserade format. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Anger en fysisk mapp där alla resurser som bilder, teckensnitt och extern CSS sparas när ett dokument exporteras till HTML. Standard är en tom sträng. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Anger namnet på mappen som används för att konstruera URI:er för alla resurser som skrivs till ett HTML-dokument. Standard är en tom sträng. |
| [get_SaveFormat](./get_saveformat/)() override | Anger formatet som dokumentet kommer att sparas i om detta spara-alternativ-objekt används. Kan vara [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) eller [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Anger om bilder skalas av Aspose.Words till den omgivande formens storlek vid export till HTML, MHTML eller EPUB. Standardvärdet är **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet är [All](../htmlelementsizeoutputmode/). |
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
| [HtmlSaveOptions](./htmlsaveoptions/)() | Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Html](../../aspose.words/saveformat/) format. |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) eller [Mobi](../../aspose.words/saveformat/) format. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sättare för [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Gör det möjligt att styra hur CSS‑stilar sparas när ett dokument sparas till HTML, MHTML eller EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Ställer in ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Gör det möjligt att styra hur dokumentdelar sparas när ett dokument sparas till HTML eller EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Gör det möjligt att styra hur teckensnitt sparas när ett dokument sparas till HTML, MHTML eller EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Gör det möjligt att styra hur bilder sparas när ett dokument sparas till HTML, MHTML eller EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Ställer in värdet som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Inställning för [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Anger om JavaScript kommer att tas bort från länkar. Standard är **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Inställning för [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Inställare för [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
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

## Exempel



Visar hur man använder en specifik kodning när man sparar ett dokument till .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Som standard kommer ett utgående .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delningskriterium låter oss segmentera dokumentet i flera HTML-delar.
// Vi kommer att ange kriterierna för att dela dokumentet i rubrikstycken.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Ange att vi vill exportera dokumentegenskaper.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Visar hur du anger mappen för lagring av länkade bilder efter att ha sparat till .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Ställ in ett alternativ för att exportera formulärfält som vanlig text istället för HTML‑inmatningselement.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Se även

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
