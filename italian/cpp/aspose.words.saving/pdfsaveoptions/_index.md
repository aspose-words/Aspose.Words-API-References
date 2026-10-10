---
title: "Aspose::Words::Saving::PdfSaveOptions classe"
linktitle: "PdfSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions classe. Può essere utilizzata per specificare opzioni aggiuntive durante il salvataggio di un documento nel formato Pdf. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Può essere usato per specificare opzioni aggiuntive durante il salvataggio di un documento nel formato [Pdf](../../aspose.words/saveformat/). Per saperne di più, visita l'articolo di documentazione [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Crea una copia profonda di questo oggetto. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione del file specificata nel nome del file fornito. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | Un flag che indica se scrivere o meno operatori aggiuntivi di posizionamento del testo. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Ottiene o imposta un valore che determina come gli allegati vengono incorporati nel documento PDF. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Ottiene o imposta un valore che determina se memorizzare nella cache o meno le grafiche posizionate nello sfondo del documento. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Restituisce un valore che determina come vengono renderizzati i colori. |
| [get_Compliance](./get_compliance/)() const | Specifica il livello di conformità agli standard PDF per i documenti di output. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Specifica se convertire i riferimenti a note a piè di pagina/note di chiusura nella storia del testo principale in collegamenti ipertestuali attivi. Quando cliccato, il collegamento ipertestuale porterà alla nota a piè di pagina/note di chiusura corrispondente. Il valore predefinito è **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Ottiene o imposta un valore che determina il modo in cui le [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) vengono esportate nel file PDF. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Ottiene o imposta i dettagli per la firma del documento PDF di output. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | Un flag che specifica se la barra del titolo della finestra deve visualizzare il titolo del documento preso dalla voce Title del dizionario delle informazioni del documento. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Ottiene un valore che determina come vengono renderizzati gli effetti 3D. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Consente di specificare le opzioni di downsample. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Controlla come i caratteri vengono incorporati nei documenti PDF risultanti. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Ottiene o imposta i dettagli per la crittografia del documento PDF di output. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Ottiene o imposta un valore che determina se esportare o meno la struttura del documento. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Ottiene o imposta un valore che determina se le forme fluttuanti vengono esportate come tag inline nella struttura del documento. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Quando **true**, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Ottiene o imposta un valore che determina se creare o meno un tag "Span" nella struttura del documento per esportare la lingua del testo. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Ottiene o imposta un valore che determina se un elemento grafico di un paragrafo deve essere contrassegnato come artefatto. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Specifica la modalità di incorporamento dei caratteri. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Specifica se generare script che emulano il comportamento specifico dei campi modulo di Microsoft Word nel PDF. Il valore predefinito è **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Determina come i segnalibri nelle intestazioni/piè di pagina vengono esportati. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Specifica come verrà selezionato lo spazio colore per le immagini nel documento PDF. |
| [get_ImageCompression](./get_imagecompression/)() const | Specifica il tipo di compressione da utilizzare per tutte le immagini nel documento. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti inchiostro (InkML). |
| [get_InterpolateImages](./get_interpolateimages/)() const | Un flag che indica se l'interpolazione delle immagini deve essere eseguita da un lettore conforme. Quando viene specificato **false**, il flag non viene scritto nel documento di output e viene utilizzato il comportamento predefinito del lettore. |
| [get_JpegQuality](./get_jpegquality/)() | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento PDF. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Ottiene il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Consente di specificare le opzioni di rendering dei metafile. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Ottiene il [NumeralFormat](../numeralformat/) utilizzato per il rendering dei numeri. Per impostazione predefinita vengono usati i numeri europei. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Ottiene o imposta un valore che determina se i collegamenti ipertestuali nel documento Pdf di output devono essere forzati ad aprirsi in una nuova finestra (o scheda) del browser. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, inoltre i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su **true**. Il valore predefinito è **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Consente di specificare le opzioni di contorno. |
| [get_PageLayout](./get_pagelayout/)() const | Specifica il layout di pagina da utilizzare quando il documento viene aperto in un lettore PDF. |
| [get_PageMode](./get_pagemode/)() const | Specifica come il documento PDF deve essere visualizzato quando aperto in un lettore PDF. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Consente di controllare come le pagine separate vengono salvate quando un documento è esportato in formato a pagina fissa. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Ottiene o imposta le pagine da renderizzare. Il valore predefinito è tutte le pagine del documento. |
| [get_PreblendImages](./get_preblendimages/)() const | Ottiene o imposta un valore che determina se pre‑mescolare le immagini trasparenti con il colore di sfondo nero. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Specifica se conservare i campi modulo di Microsoft Word come campi modulo nel PDF o convertirli in testo. Il valore predefinito è **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Quando **true**, formatta in modo leggibile l'output dove applicabile. Il valore predefinito è **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Chiamato durante il salvataggio di un documento e accetta dati sul progresso del salvataggio. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Specifica se renderizzare il bordo del campo modulo a scelta PDF. |
| [get_SaveFormat](./get_saveformat/)() override | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo [Pdf](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_TextCompression](./get_textcompression/)() const | Specifica il tipo di compressione da utilizzare per tutti i contenuti testuali nel documento. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina se gli attributi del carattere verranno modificati in base al codice del carattere utilizzato. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) viene aggiornata prima del salvataggio. Il valore predefinito è **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ottiene un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) viene aggiornata prima del salvataggio. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) viene aggiornata prima del salvataggio. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ottiene un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa a libretto, se è specificato tramite [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Ottiene o imposta un valore che determina se sostituire o meno i font TrueType Arial, Times New Roman, Courier New e Symbol con i font PDF Type 1 di base. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti). |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Specifica se utilizzare il Tag o la proprietà Id del controllo SDT come nome del campo modulo nel PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Ottiene un valore che determina quale tipo di zoom deve essere applicato quando un documento viene aperto con un visualizzatore PDF. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Ottiene un valore che determina il fattore di zoom (in percentuale) per un documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel formato [Pdf](../../aspose.words/saveformat/). |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter per [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Imposta un valore che determina come vengono renderizzati i colori. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Specifica il livello di conformità agli standard PDF per i documenti di output. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Specifica se convertire i riferimenti a note a piè di pagina/note di chiusura nella storia del testo principale in collegamenti ipertestuali attivi. Quando cliccato, il collegamento ipertestuale porterà alla nota a piè di pagina/note di chiusura corrispondente. Il valore predefinito è **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Consente di specificare le opzioni di downsample. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Consente di specificare le opzioni di rendering dei metafile. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Imposta [NumeralFormat](../numeralformat/) usato per il rendering dei numeri. Per impostazione predefinita vengono utilizzati i numeri europei. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Specifica il layout di pagina da utilizzare quando il documento viene aperto in un lettore PDF. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Specifica come il documento PDF deve essere visualizzato quando aperto in un lettore PDF. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Consente di controllare come le pagine separate vengono salvate quando un documento è esportato in formato a pagina fissa. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Imposta [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo [Pdf](../../aspose.words/saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Imposta un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Impostatore per [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Imposta un valore che determina quale tipo di zoom deve essere applicato quando un documento viene aperto con un visualizzatore PDF. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Imposta un valore che determina il fattore di zoom (in percentuale) per un documento. |
| static [Type](./type/)() |  |
## Vedi anche

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
