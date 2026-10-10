---
title: "classe Aspose::Words::Saving::HtmlFixedSaveOptions"
linktitle: "HtmlFixedSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Saving::HtmlFixedSaveOptions. Può essere usata per specificare opzioni aggiuntive quando si salva un documento nel formato HtmlFixed. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Può essere usata per specificare opzioni aggiuntive quando si salva un documento nel formato [HtmlFixed](../../aspose.words/saveformat/). Per saperne di più, visita l'articolo di documentazione [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione del file specificata nel nome del file fornito. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Restituisce un valore che determina come vengono renderizzati i colori. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Specifica il prefisso che viene aggiunto a tutti i nomi di classe nel file style.css. Il valore predefinito è **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Ottiene un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [get_Encoding](./get_encoding/)() const | Specifica la codifica da utilizzare durante l'esportazione in HTML. Il valore predefinito è **new UTF8Encoding(true)** (UTF-8 con BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Specifica se il CSS (Cascading [Style](../../aspose.words/style/) Sheet) deve essere incorporato nel documento Html. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Specifica se i caratteri devono essere incorporati nel documento Html in formato Base64. Nota: impostare questa opzione può aumentare significativamente le dimensioni del file Html di output. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Specifica se le immagini devono essere incorporate nel documento Html in formato Base64. Nota: impostare questa opzione può aumentare significativamente le dimensioni del file Html di output. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Specifica se le risorse SVG devono essere incorporate nel documento Html. Il valore predefinito è **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Ottiene o imposta l'indicazione se i campi modulo sono esportati come elementi interattivi (come tag 'input') anziché convertiti in testo o grafica. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Quando **true**, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **true**. |
| [get_FontFormat](./get_fontformat/)() const | Ottiene o imposta [ExportFontFormat](../exportfontformat/) usato per l'esportazione dei caratteri. Il valore predefinito è [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Specifica un prefisso che viene anteposto a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e nessun prefisso viene anteposto. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti inchiostro (InkML). |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Ottiene il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Consente di specificare le opzioni di rendering dei metafile. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Ottiene il [NumeralFormat](../numeralformat/) utilizzato per il rendering dei numeri. Per impostazione predefinita vengono usati i numeri europei. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, inoltre i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su **true**. Il valore predefinito è **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Specifica l'allineamento orizzontale delle pagine in un documento HTML. Il valore predefinito è [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Specifica i margini attorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o superiore a 0. Il valore predefinito è 10 punti. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Consente di controllare come le pagine separate vengono salvate quando un documento è esportato in formato a pagina fissa. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Quando **true**, formatta in modo leggibile l'output dove applicabile. Il valore predefinito è **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Chiamato durante il salvataggio di un documento e accetta dati sul progresso del salvataggio. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Consente di controllare come le risorse (immagini, caratteri e css) vengono salvate quando un documento è esportato nel formato Html a pagina fissa. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Specifica la cartella fisica in cui le risorse (immagini, caratteri, css) vengono salvate durante l'esportazione di un documento in formato Html. Il valore predefinito è **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento Html. Il valore predefinito è **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Il flag indica se le regole CSS \"@font-face\" devono essere collocate in un file separato \"fontFaces.css\" quando un documento viene salvato con un foglio di stile esterno (cioè, quando [ExportEmbeddedCss](./get_exportembeddedcss/) è **false**). Il valore predefinito è **false**, tutte le regole CSS sono scritte in un unico file \"styles.css\". |
| [get_SaveFormat](./get_saveformat/)() override | Specifica il formato in cui il documento sarà salvato se viene usato questo oggetto di opzioni di salvataggio. Può essere solo [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Specifica se il bordo attorno alle pagine deve essere mostrato. Il valore predefinito è **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina se gli attributi del carattere verranno modificati in base al codice del carattere utilizzato. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) viene aggiornata prima del salvataggio. Il valore predefinito è **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ottiene un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) viene aggiornata prima del salvataggio. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) viene aggiornata prima del salvataggio. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ottiene un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti). |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Il flag indica se i caratteri dalla macchina di destinazione devono essere usati per visualizzare il documento. Se questo flag è impostato su **true**, le proprietà [FontFormat](./get_fontformat/) e [ExportEmbeddedFonts](./get_exportembeddedfonts/) non hanno effetto, inoltre [ResourceSavingCallback](./get_resourcesavingcallback/) non viene chiamato per i caratteri. Il valore predefinito è **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter per [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Imposta un valore che determina come vengono renderizzati i colori. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | Specifica il prefisso che viene aggiunto a tutti i nomi di classe nel file style.css. Il valore predefinito è **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Setter per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Consente di specificare le opzioni di rendering dei metafile. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Imposta [NumeralFormat](../numeralformat/) usato per il rendering dei numeri. Per impostazione predefinita vengono utilizzati i numeri europei. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Consente di controllare come le pagine separate vengono salvate quando un documento è esportato in formato a pagina fissa. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Consente di controllare come le risorse (immagini, caratteri e css) vengono salvate quando un documento è esportato nel formato Html a pagina fissa. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifica il formato in cui il documento sarà salvato se viene usato questo oggetto di opzioni di salvataggio. Può essere solo [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Specifica se il bordo attorno alle pagine deve essere mostrato. Il valore predefinito è **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Imposta un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Impostatore per [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## Vedi anche

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
