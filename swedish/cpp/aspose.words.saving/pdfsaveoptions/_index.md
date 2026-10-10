---
title: "Aspose::Words::Saving::PdfSaveOptions klass"
linktitle: "PdfSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions klass. Kan användas för att ange ytterligare alternativ när ett dokument sparas i Pdf-formatet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 25000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Kan användas för att ange ytterligare alternativ när ett dokument sparas i [Pdf](../../aspose.words/saveformat/) formatet. För att lära dig mer, besök dokumentationsartikeln [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Skapar en djup klon av detta objekt. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Skapar ett spara‑alternativ‑objekt av en klass som är lämplig för det angivna spara‑formatet. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Skapar ett sparaalternativobjekt av en klass som är lämplig för filändelsen som anges i det givna filnamnet. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | En flagga som anger om ytterligare textpositioneringsoperatorer ska skrivas eller inte. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Hämtar eller anger ett booleskt värde som indikerar om inbäddning av teckensnitt med PostScript‑konturer ska tillåtas när TrueType‑teckensnitt inbäddas i ett dokument när det sparas. Standardvärdet är **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Hämtar eller anger ett värde som bestämmer hur bilagor bäddas in i PDF-dokumentet. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Hämtar eller anger ett värde som bestämmer om grafik som placerats i dokumentets bakgrund ska cachas eller inte. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Hämtar ett värde som bestämmer hur färger renderas. |
| [get_Compliance](./get_compliance/)() const | Anger PDF-standardernas efterlevnadsnivå för utdata-dokument. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Anger om fotnot-/slutnotreferenser i huvudtexten ska konverteras till aktiva hyperlänkar. När de klickas på leder hyperlänken till motsvarande fotnot/slutnot. Standard är **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Hämtar eller anger ett värde som bestämmer hur [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) exporteras till PDF-filen. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Hämtar eller anger en anpassad lokal tidszon som används för datum/tids‑fält. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Hämtar eller anger sökvägen till standardmall (inklusive filnamn). Standardvärdet för denna egenskap är **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Hämtar eller anger detaljerna för signering av utdata-PDF-dokumentet. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | En flagga som anger om fönstrets titelrad ska visa dokumenttiteln hämtad från Title-posten i dokumentinformationens katalog. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Hämtar ett värde som bestämmer hur 3D‑effekter renderas. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Hämtar eller anger ett värde som bestämmer hur DrawingML‑effekter renderas. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur DrawingML‑former renderas. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Tillåter att ange nedsamplingsalternativ. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Styr hur teckensnitt bäddas in i de resulterande PDF-dokumenten. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Hämtar eller anger detaljerna för kryptering av utdata-PDF-dokumentet. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Hämtar eller anger ett värde som bestämmer om dokumentstrukturen ska exporteras eller inte. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Hämtar eller anger ett värde som bestämmer om flytande former exporteras som inline-taggar i dokumentstrukturen. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | När **true** görs namn och version av Aspose.Words inbäddade i de skapade filerna. Standardvärdet är **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Hämtar eller anger ett värde som bestämmer om ett \"Span\"-tagg ska skapas i dokumentstrukturen för att exportera textspråket eller inte. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Hämtar eller anger ett värde som bestämmer om en stycke-grafik ska markeras som ett artefakt. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Anger teckensnittsinbäddningsläget. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Anger om skript ska genereras som efterliknar specifikt Microsoft Word-formulärfältbeteende i PDF. Standard är **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Bestämmer hur bokmärken i sidhuvuden/sidfötter exporteras. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Anger hur färgrymden kommer att väljas för bilderna i PDF-dokumentet. |
| [get_ImageCompression](./get_imagecompression/)() const | Anger komprimeringstyp som ska användas för alla bilder i dokumentet. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas. |
| [get_InterpolateImages](./get_interpolateimages/)() const | En flagga som indikerar om bildinterpolering ska utföras av en kompatibel läsare. När **false** anges skrivs inte flaggan till utdatafilen och läsarens standardbeteende används istället. |
| [get_JpegQuality](./get_jpegquality/)() | Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG-bilder i PDF-dokumentet. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Hämtar eller anger ett värde som bestämmer kvaliteten på JPEG‑bilderna i ett Html‑dokument. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Hämtar värdet som bestämmer om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Tillåter att ange renderingsalternativ för metafiler. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Hämtar [NumeralFormat](../numeralformat/) som används för rendering av siffror. Europeiska siffror används som standard. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Hämtar eller anger ett värde som bestämmer om hyperlänkar i utdata‑Pdf‑dokumentet tvingas öppnas i ett nytt fönster (eller flik) i en webbläsare. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Flaggan indikerar om det krävs att optimera utdata. Om denna flagga är satt tas överflödiga nästlade dukar och tomma dukar bort, även närliggande glyfer med samma formatering slås ihop. Obs: Noggrannheten i innehållsvisningen kan påverkas om denna egenskap är satt till **true**. Standard är **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Tillåter att ange konturalternativ. |
| [get_PageLayout](./get_pagelayout/)() const | Anger sidlayouten som ska användas när dokumentet öppnas i en PDF-läsare. |
| [get_PageMode](./get_pagemode/)() const | Anger hur PDF-dokumentet ska visas när det öppnas i en PDF-läsare. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Tillåter att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Hämtar eller anger sidorna som ska renderas. Standard är alla sidor i dokumentet. |
| [get_PreblendImages](./get_preblendimages/)() const | Hämtar eller anger ett värde som bestämmer om transparenta bilder ska förblandas med svart bakgrundsfärg eller inte. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Anger om Microsoft Word-formulärfält ska bevaras som formulärfält i PDF eller konverteras till text. Standard är **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | När **true**, formaterar output snyggt där det är tillämpligt. Standardvärdet är **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Kallas under sparande av ett dokument och accepterar data om sparningsförloppet. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Anger om PDF‑valformulärfältets kantlinje ska renderas. |
| [get_SaveFormat](./get_saveformat/)() override | Anger formatet som dokumentet sparas i om detta spara‑alternativ‑objekt används. Kan endast vara [Pdf](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Anger mappen för temporära filer som används vid sparande till en DOC- eller DOCX-fil. Som standard är denna egenskap **null** och inga temporära filer används. |
| [get_TextCompression](./get_textcompression/)() const | Anger komprimeringstyp som ska användas för allt textinnehåll i dokumentet. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Bestämmer om teckensnittsattributen ska ändras enligt den teckenkod som används. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) uppdateras före sparande. Standardvärdet är **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Hämtar ett värde som bestämmer om fält av vissa typer ska uppdateras före sparande av dokumentet till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) uppdateras före sparande. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Hämtar eller anger ett värde som bestämmer om egenskapen [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) uppdateras före sparande. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Hämtar ett värde som bestämmer om presentationsbilden för OLE-kontroller kommer att uppdateras. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Hämtar eller anger ett värde som bestämmer om anti-aliasing ska användas för rendering. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Hämtar eller anger ett booleskt värde som indikerar om dokumentet ska sparas med en boktryckningslayout, om det anges via [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Hämtar eller anger ett värde som bestämmer om TrueType‑typsnitten Arial, Times New Roman, Courier New och Symbol ska ersättas med PDF:s kärn‑Type 1‑typsnitt eller inte. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Hämtar eller anger ett värde som bestämmer om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas. |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Anger om SDT‑kontrollens Tag‑ eller Id‑egenskap ska användas som namn på formulärfält i PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Hämtar ett värde som bestämmer vilken typ av zoom som ska tillämpas när ett dokument öppnas med en PDF‑visare. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Hämtar ett värde som bestämmer zoomfaktor (i procent) för ett dokument. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument i [Pdf](../../aspose.words/saveformat/)-format. |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sättare för [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Anger ett värde som bestämmer hur färger renderas. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Anger PDF-standardernas efterlevnadsnivå för utdata-dokument. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Anger om fotnot-/slutnotreferenser i huvudtexten ska konverteras till aktiva hyperlänkar. När de klickas på leder hyperlänken till motsvarande fotnot/slutnot. Standard är **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Ställer in ett värde som bestämmer hur 3D‑effekter renderas. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Inställare för [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Tillåter att ange nedsamplingsalternativ. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Ställer in värdet som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för denna egenskap är **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Tillåter att ange renderingsalternativ för metafiler. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Anger [NumeralFormat](../numeralformat/) som används för rendering av siffror. Europeiska siffror används som standard. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Sättare för [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Anger sidlayouten som ska användas när dokumentet öppnas i en PDF-läsare. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Anger hur PDF-dokumentet ska visas när det öppnas i en PDF-läsare. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Tillåter att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Sättare för [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Inställning för [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Inställning för [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Anger formatet som dokumentet sparas i om detta spara‑alternativ‑objekt används. Kan endast vara [Pdf](../../aspose.words/saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Inställare för [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Anger ett värde som bestämmer om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för denna egenskap är **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Anger ett värde som bestämmer om presentationsbilden för OLE‑kontroller ska uppdateras. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Inställare för [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Sättare för [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Anger ett värde som bestämmer vilken typ av zoom som ska tillämpas när ett dokument öppnas med en PDF‑visare. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Anger ett värde som bestämmer zoomfaktorn (i procent) för ett dokument. |
| static [Type](./type/)() |  |
## Se även

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
