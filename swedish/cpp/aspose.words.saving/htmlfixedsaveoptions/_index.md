---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions-klass"
linktitle: "HtmlFixedSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions-klass. Kan användas för att ange ytterligare alternativ när ett dokument sparas i HtmlFixed-formatet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Kan användas för att ange ytterligare alternativ när ett dokument sparas i [HtmlFixed](../../aspose.words/saveformat/) formatet. För att lära dig mer, besök dokumentationsartikeln [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Skapar ett spara‑alternativ‑objekt av en klass som är lämplig för det angivna spara‑formatet. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Skapar ett sparaalternativobjekt av en klass som är lämplig för filändelsen som anges i det givna filnamnet. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Hämtar eller anger ett booleskt värde som indikerar om inbäddning av teckensnitt med PostScript‑konturer ska tillåtas när TrueType‑teckensnitt inbäddas i ett dokument när det sparas. Standardvärdet är **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Hämtar ett värde som bestämmer hur färger renderas. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Anger prefix som läggs till alla klassnamn i style.css-filen. Standardvärdet är **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Hämtar eller anger en anpassad lokal tidszon som används för datum/tids‑fält. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Hämtar eller anger sökvägen till standardmall (inklusive filnamn). Standardvärdet för denna egenskap är **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Hämtar ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Hämtar eller anger ett värde som bestämmer hur DrawingML‑effekter renderas. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur DrawingML‑former renderas. |
| [get_Encoding](./get_encoding/)() const | Anger kodningen som ska användas vid export till HTML. Standardvärdet är **new UTF8Encoding(true)** (UTF-8 med BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Anger om CSS (Cascading [Style](../../aspose.words/style/) Sheet) ska bäddas in i Html-dokumentet. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Anger om teckensnitt ska bäddas in i Html-dokumentet i Base64-format. Observera att inställning av denna flagga kan avsevärt öka storleken på den genererade Html-filen. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Anger om bilder ska bäddas in i Html-dokumentet i Base64-format. Observera att inställning av denna flagga kan avsevärt öka storleken på den genererade Html-filen. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Anger om SVG-resurser ska bäddas in i Html-dokumentet. Standardvärdet är **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Hämtar eller anger indikation på om formulärfält exporteras som interaktiva objekt (som 'input'-tagg) snarare än att konverteras till text eller grafik. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | När **true** görs namn och version av Aspose.Words inbäddade i de skapade filerna. Standardvärdet är **true**. |
| [get_FontFormat](./get_fontformat/)() const | Hämtar eller anger [ExportFontFormat](../exportfontformat/) som används för teckensnittsexport. Standardvärdet är [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Anger ett prefix som läggs före alla genererade element-ID:n i utmatningsdokumentet. Standardvärdet är null och inget prefix läggs till. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG‑bilderna i ett Html‑dokument. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Hämtar värdet som bestämmer om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Tillåter att ange renderingsalternativ för metafiler. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Hämtar [NumeralFormat](../numeralformat/) som används för rendering av siffror. Europeiska siffror används som standard. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Flaggan indikerar om det krävs att optimera utdata. Om denna flagga är satt tas överflödiga nästlade dukar och tomma dukar bort, även intilliggande glyfer med samma formatering konkateneras. Observera: Noggrannheten i innehållsvisningen kan påverkas om denna egenskap är satt till **true**. Standard är **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Anger den horisontella justeringen av sidor i ett HTML-dokument. Standardvärdet är [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Anger marginalerna runt sidor i ett HTML-dokument. Marginalvärdet mäts i punkter och bör vara lika med eller större än 0. Standardvärdet är 10 punkter. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Tillåter att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Hämtar eller anger sidorna som ska renderas. Standard är alla sidor i dokumentet. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | När **true**, formaterar output snyggt där det är tillämpligt. Standardvärdet är **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Kallas under sparande av ett dokument och accepterar data om sparningsförloppet. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Anger om JavaScript kommer att tas bort från länkar. Standard är **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Gör det möjligt att kontrollera hur resurser (bilder, teckensnitt och css) sparas när ett dokument exporteras till fast sidformat Html. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Anger den fysiska mappen där resurser (bilder, teckensnitt, css) sparas när ett dokument exporteras till Html-format. Standard är **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett Html-dokument. Standardvärdet är **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Flaggan indikerar om "@font-face"-CSS-regler ska placeras i en separat fil "fontFaces.css" när ett dokument sparas med extern stilmall (det vill säga när [ExportEmbeddedCss](./get_exportembeddedcss/) är **false**). Standardvärdet är **false**, alla CSS-regler skrivs till en enda fil "styles.css". |
| [get_SaveFormat](./get_saveformat/)() override | Anger det format som dokumentet kommer att sparas i om detta spara-alternativobjekt används. Kan endast vara [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Anger om kantlinjen runt sidorna ska visas. Standard är **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Anger mappen för temporära filer som används vid sparande till en DOC- eller DOCX-fil. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Bestämmer om teckensnittsattributen ska ändras enligt den teckenkod som används. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) uppdateras före sparande. Standardvärdet är **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Hämtar ett värde som bestämmer om fält av vissa typer ska uppdateras före sparande av dokumentet till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) uppdateras före sparande. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) uppdateras före sparande. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Hämtar ett värde som bestämmer om presentationsbilden för OLE-kontroller kommer att uppdateras. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Hämtar eller anger ett värde som bestämmer om anti-aliasing ska användas för rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Hämtar eller anger ett värde som bestämmer om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas. |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Flaggan indikerar om teckensnitt från målmaskinen måste användas för att visa dokumentet. Om denna flagga är satt till **true** har [FontFormat](./get_fontformat/) och [ExportEmbeddedFonts](./get_exportembeddedfonts/) egenskaper ingen effekt, och även [ResourceSavingCallback](./get_resourcesavingcallback/) utlöses inte för teckensnitt. Standard är **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sättare för [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Anger ett värde som bestämmer hur färger renderas. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | Anger prefix som läggs till alla klassnamn i style.css-filen. Standardvärdet är **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Ställer in ett värde som bestämmer hur 3D‑effekter renderas. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Sättare för [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Ställer in värdet som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Tillåter att ange renderingsalternativ för metafiler. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Anger [NumeralFormat](../numeralformat/) som används för rendering av siffror. Europeiska siffror används som standard. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Tillåter att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Sättare för [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Inställning för [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Gör det möjligt att kontrollera hur resurser (bilder, teckensnitt och css) sparas när ett dokument exporteras till fast sidformat Html. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Anger det format som dokumentet kommer att sparas i om detta spara-alternativobjekt används. Kan endast vara [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Anger om kantlinjen runt sidorna ska visas. Standard är **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Anger ett värde som bestämmer om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Anger ett värde som bestämmer om presentationsbilden för OLE‑kontroller ska uppdateras. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Sättare för [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## Se även

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
