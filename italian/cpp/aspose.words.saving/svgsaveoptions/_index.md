---
title: "Aspose::Words::Saving::SvgSaveOptions class"
linktitle: "SvgSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SvgSaveOptions class. Può essere usato per specificare opzioni aggiuntive quando si salva un documento nel formato Svg. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class


Può essere usato per specificare opzioni aggiuntive quando si salva un documento nel formato [Svg](../../aspose.words/saveformat/). Per saperne di più, visita l'articolo di documentazione [Specificare le opzioni di salvataggio](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class SvgSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione del file specificata nel nome del file fornito. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Restituisce un valore che determina come vengono renderizzati i colori. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Ottiene un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Specifica se le immagini devono essere incorporate nel documento SVG come base64. Tieni presente che l'attivazione di questa opzione può comportare un aumento significativo delle dimensioni del file SVG di output. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Quando **true**, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **true**. |
| [get_FitToViewPort](./get_fittoviewport/)() const | Specifica se l'SVG di output deve riempire l'area disponibile del viewport (finestra del browser o contenitore). Quando impostato su **true**, larghezza e altezza dell'SVG di output sono impostate al 100%. Il valore predefinito è **false**. |
| [get_IdPrefix](./get_idprefix/)() const | Specifica un prefisso che viene anteposto a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e nessun prefisso viene anteposto. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti inchiostro (InkML). |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html. |
| [get_MaxImageResolution](./get_maximageresolution/)() const | Ottiene o imposta un valore in pixel per pollice che limita la risoluzione delle immagini raster esportate. Il valore predefinito è zero. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Ottiene il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Consente di specificare le opzioni di rendering dei metafile. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Ottiene il [NumeralFormat](../numeralformat/) utilizzato per il rendering dei numeri. Per impostazione predefinita vengono usati i numeri europei. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, inoltre i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su **true**. Il valore predefinito è **false**. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Consente di controllare come le pagine separate vengono salvate quando un documento è esportato in formato a pagina fissa. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Quando **true**, formatta in modo leggibile l'output dove applicabile. Il valore predefinito è **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Chiamato durante il salvataggio di un documento e accetta dati sul progresso del salvataggio. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è **false**. Se questa opzione è abilitata, tutti i collegamenti contenenti JavaScript saranno sostituiti con "javascript:void(0)". |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Consente di controllare come le risorse (immagini) vengono salvate quando un documento viene esportato in formato SVG. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Specifica la cartella fisica in cui le risorse (immagini) vengono salvate durante l'esportazione di un documento in formato SVG. Il valore predefinito è **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento SVG. Il valore predefinito è **null**. |
| [get_SaveFormat](./get_saveformat/)() override | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo [Svg](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Controlla se un bordo viene aggiunto al contorno della pagina. Il valore predefinito è **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_TextOutputMode](./get_textoutputmode/)() const | Ottiene o imposta un valore che determina come il testo deve essere renderizzato in SVG. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina se gli attributi del carattere verranno modificati in base al codice del carattere utilizzato. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) viene aggiornata prima del salvataggio. Il valore predefinito è **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ottiene un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) viene aggiornata prima del salvataggio. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) viene aggiornata prima del salvataggio. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ottiene un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter per [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Imposta un valore che determina come vengono renderizzati i colori. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Specifica se le immagini devono essere incorporate nel documento SVG come base64. Tieni presente che l'attivazione di questa opzione può comportare un aumento significativo delle dimensioni del file SVG di output. |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FitToViewPort](./set_fittoviewport/)(bool) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort](./get_fittoviewport/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MaxImageResolution](./set_maximageresolution/)(int32_t) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution](./get_maximageresolution/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Consente di specificare le opzioni di rendering dei metafile. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Imposta [NumeralFormat](../numeralformat/) usato per il rendering dei numeri. Per impostazione predefinita vengono utilizzati i numeri europei. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Consente di controllare come le pagine separate vengono salvate quando un documento è esportato in formato a pagina fissa. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Consente di controllare come le risorse (immagini) vengono salvate quando un documento viene esportato in formato SVG. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo [Svg](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder](./get_showpageborder/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextOutputMode](./set_textoutputmode/)(Aspose::Words::Saving::SvgTextOutputMode) | Setter per [Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode](./get_textoutputmode/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Imposta un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [SvgSaveOptions](./svgsaveoptions/)() |  |
| static [Type](./type/)() |  |
## Vedi anche

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
