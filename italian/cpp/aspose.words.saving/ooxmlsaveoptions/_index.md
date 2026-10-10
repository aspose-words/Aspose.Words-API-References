---
title: "Classe Aspose::Words::Saving::OoxmlSaveOptions"
linktitle: "OoxmlSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Saving::OoxmlSaveOptions. Può essere usata per specificare opzioni aggiuntive quando si salva un documento nei formati Docx, Docm, Dotx, Dotm o FlatOpc. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class


Può essere usata per specificare opzioni aggiuntive quando si salva un documento nei formati [Docx](../../aspose.words/saveformat/), [Docm](../../aspose.words/saveformat/), [Dotx](../../aspose.words/saveformat/), [Dotm](../../aspose.words/saveformat/) o [FlatOpc](../../aspose.words/saveformat/). Per saperne di più, visita l'articolo di documentazione [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class OoxmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione del file specificata nel nome del file fornito. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è **false**. |
| [get_Compliance](./get_compliance/)() | Specifica la versione OOXML per il documento di output. Il valore predefinito è [Ecma376_2006](../ooxmlcompliance/). |
| [get_CompressionLevel](./get_compressionlevel/)() const | Specifica il livello di compressione utilizzato per salvare il documento. Il valore predefinito è [Normal](../compressionlevel/). |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Ottiene o imposta l'oggetto [DigitalSignatureDetails](../digitalsignaturedetails/) utilizzato per firmare un documento. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Ottiene un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Quando **true**, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti inchiostro (InkML). |
| [get_KeepLegacyControlChars](./get_keeplegacycontrolchars/)() const | Mantiene la rappresentazione originale dei caratteri di controllo legacy. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Ottiene il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [get_Password](./get_password/)() const | Ottiene/imposta una password per crittografare il documento usando l'algoritmo di crittografia ECMA376 Standard. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Quando **true**, formatta in modo leggibile l'output dove applicabile. Il valore predefinito è **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Chiamato durante il salvataggio di un documento e accetta dati sul progresso del salvataggio. |
| [get_SaveFormat](./get_saveformat/)() override | Specifica il formato in cui il documento verrà salvato se viene usato questo oggetto di opzioni di salvataggio. Può essere [Docx](../../aspose.words/saveformat/), [Docm](../../aspose.words/saveformat/), [Dotx](../../aspose.words/saveformat/), [Dotm](../../aspose.words/saveformat/) o [FlatOpc](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina se gli attributi del carattere verranno modificati in base al codice del carattere utilizzato. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) viene aggiornata prima del salvataggio. Il valore predefinito è **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Ottiene un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) viene aggiornata prima del salvataggio. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Ottiene o imposta un valore che determina se la proprietà [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) viene aggiornata prima del salvataggio. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Ottiene un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti). |
| [get_Zip64Mode](./get_zip64mode/)() const | Specifica se utilizzare o meno le estensioni del formato ZIP64 per il documento di output. Il valore predefinito è [Never](../zip64mode/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OoxmlSaveOptions](./ooxmlsaveoptions/)() | Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato [Docx](../../aspose.words/saveformat/). |
| [OoxmlSaveOptions](./ooxmlsaveoptions/)(Aspose::Words::SaveFormat) | Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nei formati [Docx](../../aspose.words/saveformat/), [Docm](../../aspose.words/saveformat/), [Dotx](../../aspose.words/saveformat/), [Dotm](../../aspose.words/saveformat/) o [FlatOpc](../../aspose.words/saveformat/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter per [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::OoxmlCompliance) | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance](./get_compliance/). |
| [set_CompressionLevel](./set_compressionlevel/)(Aspose::Words::Saving::CompressionLevel) | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel](./get_compressionlevel/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter per [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::DigitalSignatureDetails\>\&) | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_KeepLegacyControlChars](./set_keeplegacycontrolchars/)(bool) | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars](./get_keeplegacycontrolchars/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è **false**. |
| [set_Password](./set_password/)(const System::String\&) | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_Password](./get_password/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato a pagina fissa. Il valore predefinito per questa proprietà è **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Imposta un valore che determina se l'immagine di presentazione dei controlli OLE verrà aggiornata. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Impostatore per [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_Zip64Mode](./set_zip64mode/)(Aspose::Words::Saving::Zip64Mode) | Metodo set per [Aspose::Words::Saving::OoxmlSaveOptions::get_Zip64Mode](./get_zip64mode/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come impostare una specifica di conformità OOXML a cui aderire per un documento salvato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se configuriamo le opzioni di compatibilità per conformarci a Microsoft Word 2003,
// l'inserimento di un'immagine definirà la sua forma usando VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Lo standard OOXML "ISO/IEC 29500:2008" non supporta forme VML.
// Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
// qualsiasi documento che salviamo passando questo oggetto dovrà seguire tale standard.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Il nostro documento salvato definisce la forma usando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## Vedi anche

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
