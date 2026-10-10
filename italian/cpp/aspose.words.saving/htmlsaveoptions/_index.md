---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions class. Può essere usata per specificare opzioni aggiuntive quando si salva un documento nei formati Html, Mhtml, Epub, Azw3 o Mobi. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Può essere usata per specificare opzioni aggiuntive quando si salva un documento nei formati [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) o [Mobi](../../aspose.words/saveformat/). Per saperne di più, visita l'articolo di documentazione [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione del file specificata nel nome del file fornito. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Specifica se gli rientri negativi sinistro e destro dei paragrafi sono normalizzati durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Specifica un prefisso che viene aggiunto a tutti i nomi delle classi CSS. Il valore predefinito è una stringa vuota e i nomi delle classi CSS generate non hanno alcun prefisso comune. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Consente di controllare come vengono salvati gli stili CSS quando un documento viene salvato in HTML, MHTML o EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Specifica il percorso e il nome del file Cascading [Style](../../aspose.words/style/) Sheet (CSS) scritto quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Specifica come gli stili CSS (Cascading [Style](../../aspose.words/style/) Sheet) vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è [Inline](../cssstylesheettype/) per HTML/MHTML e [External](../cssstylesheettype/) per EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Ottiene un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Consente di controllare come le parti del documento vengono salvate quando un documento è salvato in HTML o EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Specifica come il documento deve essere suddiviso durante il salvataggio nei formati [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) o [Azw3](../../aspose.words/saveformat/). Il valore predefinito è [None](../documentsplitcriteria/) per HTML e [HeadingParagraph](../documentsplitcriteria/) per EPUB e AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Specifica il livello massimo di intestazioni al quale suddividere il documento. Il valore predefinito è **%2**. |
| [get_Encoding](./get_encoding/)() const | Specifica la codifica da utilizzare durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è **new UTF8Encoding(false)** (UTF-8 senza BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Specifica se utilizzare URL CID (Content-ID) per fare riferimento alle risorse (immagini, font, CSS) incluse nei documenti MHTML. Il valore predefinito è **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Specifica se esportare le proprietà del documento predefinite e personalizzate in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Controlla come i campi modulo a discesa vengono salvati in HTML o MHTML. Il valore predefinito è **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Specifica se le risorse dei font devono essere esportate in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Specifica se le risorse dei font devono essere incorporate in HTML con codifica Base64. Il valore predefinito è **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Quando **true**, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è [PerSection](../exportheadersfootersmode/) per HTML/MHTML e [None](../exportheadersfootersmode/) per EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Specifica se le immagini vengono salvate in formato Base64 nell'HTML, MHTML o EPUB di output. Il valore predefinito è **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Specifica se le informazioni sulla lingua vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Controlla come le etichette delle liste vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Specifica se l'URL originale deve essere utilizzato come URL delle immagini collegate. Il valore predefinito è **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Specifica se i margini della pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Specifica se la configurazione della pagina viene esportata in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Specifica se le dimensioni dei caratteri devono essere emesse in unità relative durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Specifica se scrivere le informazioni di roundtrip durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **true** per HTML e **false** per MHTML e EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Controlla se i nodi [Shape](../../aspose.words.drawing/shape/) vengono convertiti in immagini SVG durante il salvataggio in HTML, MHTML, EPUB o AZW3. Il valore predefinito è **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Controlla come i campi di modulo di input di testo vengono salvati in HTML o MHTML. Il valore predefinito è **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Specifica se scrivere i numeri di pagina nel sommario durante il salvataggio in HTML, MHTML e EPUB. Il valore predefinito è **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Specifica se scrivere la dichiarazione DOCTYPE durante il salvataggio in HTML o MHTML. Quando **true**, scrive una dichiarazione DOCTYPE nel documento prima dell'elemento radice. Il valore predefinito è **false**. Quando si salva in EPUB o HTML5 ([Html5](../htmlversion/)) la dichiarazione DOCTYPE viene sempre scritta. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Controlla quali risorse di carattere richiedono il subset durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Consente di controllare come i caratteri vengono salvati quando un documento è salvato in HTML, MHTML o EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Specifica la cartella fisica in cui i caratteri vengono salvati durante l'esportazione di un documento in HTML. Il valore predefinito è una stringa vuota. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Specifica il nome della cartella usata per costruire gli URI dei caratteri scritti in un documento HTML. Il valore predefinito è una stringa vuota. |
| [get_HtmlVersion](./get_htmlversion/)() const | Specifica la versione dello standard HTML da utilizzare quando si salva il documento in HTML o MHTML. Il valore predefinito è [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Consente di controllare come le immagini vengono salvate quando un documento è salvato in HTML, MHTML o EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Specifica la cartella fisica in cui le immagini vengono salvate durante l'esportazione di un documento in formato HTML. Il valore predefinito è una stringa vuota. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento HTML. Il valore predefinito è una stringa vuota. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti inchiostro (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Ottiene il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Specifica in quale formato vengono salvati i metafile durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è [Png](../htmlmetafileformat/), il che significa che i metafile vengono renderizzati in immagini raster PNG. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Specifica il livello massimo di intestazioni popolato nella mappa di navigazione durante l'esportazione nei formati EPUB, MOBI o AZW3. Il valore predefinito è **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Controlla come gli oggetti OfficeMath vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Quando **true**, formatta in modo leggibile l'output dove applicabile. Il valore predefinito è **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Chiamato durante il salvataggio di un documento e accetta dati sul progresso del salvataggio. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Specifica se i caratteri backslash devono essere sostituiti con i simboli yen. Il valore predefinito è **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Specifica se i nomi delle famiglie di caratteri utilizzati nel documento vengono risolti e sostituiti secondo [FontSettings](../../aspose.words/document/get_fontsettings/) quando vengono scritti in formati basati su HTML. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Specifica una cartella fisica in cui tutte le risorse come immagini, caratteri e CSS esterni vengono salvate quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Specifica il nome della cartella utilizzata per costruire gli URI di tutte le risorse scritte in un documento HTML. Il valore predefinito è una stringa vuota. |
| [get_SaveFormat](./get_saveformat/)() override | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) o [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Specifica se le immagini vengono ridimensionate da Aspose.Words alle dimensioni della forma di contenimento durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Controlla come le larghezze di tabelle, righe e celle vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è [All](../htmlelementsizeoutputmode/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina se gli attributi del carattere verranno modificati in base al codice del carattere utilizzato. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) viene aggiornata prima del salvataggio. Il valore predefinito è **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ottiene un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) viene aggiornata prima del salvataggio. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) viene aggiornata prima del salvataggio. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ottiene un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti). |
| [GetType](./gettype/)() const override |  |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel formato [Html](../../aspose.words/saveformat/). |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nei formati [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) o [Mobi](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter per [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Setter per [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Setter per [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Consente di controllare come vengono salvati gli stili CSS quando un documento viene salvato in HTML, MHTML o EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Setter per [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Setter per [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Consente di controllare come le parti del documento vengono salvate quando un documento è salvato in HTML o EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Consente di controllare come i caratteri vengono salvati quando un documento è salvato in HTML, MHTML o EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Consente di controllare come le immagini vengono salvate quando un documento è salvato in HTML, MHTML o EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Impostatore per [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Imposta un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come utilizzare una codifica specifica durante il salvataggio di un documento in .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilizza un oggetto SaveOptions per specificare la codifica di un documento che salveremo.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Per impostazione predefinita, un documento di output .epub avrà tutti i suoi contenuti in un'unica parte HTML.
// Un criterio di divisione ci consente di segmentare il documento in diverse parti HTML.
// Imposteremo i criteri per dividere il documento in paragrafi di intestazione.
// Questo è utile per i lettori che non possono leggere file HTML più grandi di una dimensione specifica.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Specifica che desideriamo esportare le proprietà del documento.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Mostra come specificare la cartella per memorizzare le immagini collegate dopo il salvataggio in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Imposta un'opzione per esportare i campi modulo come testo semplice invece di elementi di input HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Vedi anche

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
