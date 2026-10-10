---
title: "Classe Aspose::Words::Document"
linktitle: "Documento"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Document. Rappresenta un documento Word. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words/document/
---
## Document class


Rappresenta un documento Word. Per saperne di più, visita l'articolo di documentazione [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Accetta tutte le modifiche tracciate nel documento. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del documento. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del documento. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Aggiunge il documento specificato alla fine di questo documento. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Aggiunge il documento specificato alla fine di questo documento. |
| [Cleanup](./cleanup/)() | Rimuove gli stili e le liste inutilizzati dal documento. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Rimuove gli stili e le liste inutilizzati dal documento in base alle [CleanupOptions](../cleanupoptions/) fornite. |
| [Clone](./clone/)() | Esegue una copia profonda del [Document](./). |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Confronta questo documento con un altro documento producendo modifiche come numero di revisioni di modifica e formattazione [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta questo documento con un altro documento producendo modifiche come numero di revisioni di modifica e formattazione [Revision](../revision/). Consente di specificare le opzioni di confronto utilizzando [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Copia gli stili dal modello specificato a un documento. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Copia gli stili dal modello specificato a un documento. |
| [Document](./document/)() | Crea un documento Word vuoto. |
| [Document](./document/)(const System::String\&) | Apre un documento esistente da un file. Rileva automaticamente il formato del file. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Apre un documento esistente da un file. Consente di specificare opzioni aggiuntive come una password di crittografia. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Apre un documento esistente da uno stream. Rileva automaticamente il formato del file. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Apre un documento esistente da uno stream. Consente di specificare opzioni aggiuntive come una password di crittografia. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Se il documento non contiene sezioni, crea una sezione con un paragrafo. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Converte la formattazione specificata negli stili di tabella in formattazione diretta sulle tabelle nel documento. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Restituisce l'oggetto [Document](./) che rappresenta l'intervallo di pagine specificato e le opzioni di estrazione della pagina fornite. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Restituisce l'oggetto [Document](./) che rappresenta l'intervallo di pagine specificato. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Ottiene o imposta il percorso completo del modello allegato al documento. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Ottiene o imposta un flag che indica se gli stili nel documento vengono aggiornati per corrispondere agli stili del modello allegato ogni volta che il documento viene aperto in MS Word. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Ottiene o imposta la forma di sfondo del documento. Può essere **null**. |
| [get_Bibliography](./get_bibliography/)() | Ottiene l'oggetto [Bibliography](./get_bibliography/) che rappresenta l'elenco delle fonti disponibili nel documento. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Restituisce una raccolta che rappresenta tutte le proprietà integrate del documento. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Fornisce l'accesso alle opzioni di compatibilità del documento (cioè le preferenze dell'utente inserite nella scheda **Compatibility** della finestra di dialogo **Options** in Word). |
| [get_Compliance](./get_compliance/)() | Ottiene la versione di conformità OOXML determinata dal contenuto del documento caricato. Ha senso solo per i documenti OOXML. |
| [get_Count](../compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Restituisce una raccolta che rappresenta tutte le proprietà personalizzate del documento. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Ottiene o imposta la raccolta di Custom XML Data Storage Parts. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Ottiene o imposta l'intervallo (in punti) tra le tabulazioni predefinite. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Ottiene la raccolta delle firme digitali per questo documento e i relativi risultati di convalida. |
| [get_Document](../documentbase/get_document/)() const override | Ottiene questa istanza. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Fornisce le opzioni che controllano la numerazione e il posizionamento delle note finali in questo documento. |
| [get_FieldOptions](./get_fieldoptions/)() | Ottiene un oggetto [FieldOptions](../../aspose.words.fields/fieldoptions/) che rappresenta le opzioni per controllare la gestione dei campi nel documento. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FirstSection](./get_firstsection/)() | Ottiene la prima sezione del documento. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento. |
| [get_FontSettings](./get_fontsettings/)() const | Ottiene o imposta le impostazioni dei caratteri del documento. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Fornisce le opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questo documento. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Fornisce l'accesso ai separatori di note a piè di pagina/note finali definiti nel documento. |
| [get_Frameset](./get_frameset/)() const | Restituisce un'istanza [Frameset](./get_frameset/) se questo documento rappresenta una pagina con frame. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Ottiene o imposta il documento glossario all'interno di questo documento o modello. Un documento glossario è un archivio per le voci AutoText, AutoCorrect e Building Block definite in un documento. |
| [get_GrammarChecked](./get_grammarchecked/)() | Restituisce **true** se il documento è stato controllato per la grammatica. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_HasMacros](./get_hasmacros/)() | Restituisce **true** se il documento contiene un progetto VBA (macro). |
| [get_HasRevisions](./get_hasrevisions/)() | Restituisce **true** se il documento ha modifiche tracciate. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Fornisce l'accesso alle opzioni di sillabazione del documento. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Specifica se includere caselle di testo, note a piè di pagina e note finali nelle statistiche del conteggio parole. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_JustificationMode](./get_justificationmode/)() | Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_LastSection](./get_lastsection/)() | Ottiene l'ultima sezione del documento. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Ottiene un oggetto [LayoutOptions](../../aspose.words.layout/layoutoptions/) che rappresenta le opzioni per controllare il processo di layout di questo documento. |
| [get_Lists](../documentbase/get_lists/)() const | Fornisce l'accesso alla formattazione delle liste utilizzata nel documento. |
| [get_MailMerge](./get_mailmerge/)() | Restituisce un oggetto [MailMerge](../../aspose.words.mailmerging/mailmerge/) che rappresenta la funzionalità di stampa unione per il documento. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Ottiene o imposta l'oggetto che contiene tutte le informazioni di stampa unione per un documento. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | Ottiene il nome file originale del documento. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Ottiene il formato del documento originale che è stato caricato in questo oggetto. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Ottiene o imposta la raccolta di parti personalizzate (contenuto arbitrario) che sono collegate al pacchetto OOXML usando "relazioni sconosciute". |
| [get_PageColor](../documentbase/get_pagecolor/)() | Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione semplificata di [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | Ottiene il numero di pagine del documento calcolato dall'ultima operazione di layout della pagina. |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Ottiene il tipo di protezione del documento attualmente attivo. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Specifica se la kerning si applica sia al testo latino sia alla punteggiatura. |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Fornisce informazioni sul punteggio di leggibilità per il documento. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Ottiene o imposta un flag che indica che Microsoft Word rimuoverà tutte le informazioni utente da commenti, revisioni e proprietà del documento al salvataggio del documento. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Consente di controllare come vengono caricate le risorse esterne. |
| [get_Revisions](./get_revisions/)() | Ottiene una raccolta di revisioni (modifiche tracciate) presenti in questo documento. |
| [get_RevisionsView](./get_revisionsview/)() const | Ottiene o imposta un valore che indica se lavorare con la versione originale o revisionata di un documento. |
| [get_Sections](./get_sections/)() | Restituisce una raccolta che rappresenta tutte le sezioni del documento. |
| [get_ShadeFormData](./get_shadeformdata/)() | Specifica se attivare l'ombreggiatura grigia sui campi modulo. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Specifica se visualizzare gli errori grammaticali in questo documento. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Specifica se visualizzare gli errori ortografici in questo documento. |
| [get_SpellingChecked](./get_spellingchecked/)() | Restituisce **true** se il documento è stato controllato per l'ortografia. |
| [get_Styles](../documentbase/get_styles/)() const | Restituisce una raccolta di stili definiti nel documento. |
| [get_Theme](./get_theme/)() | Ottiene l'oggetto [Theme](./get_theme/) per questo documento. |
| [get_TrackRevisions](./get_trackrevisions/)() | Vero se le modifiche sono tracciate quando questo documento viene modificato in Microsoft Word. |
| [get_Variables](./get_variables/)() | Restituisce la raccolta di variabili aggiunte a un documento o modello. |
| [get_VbaProject](./get_vbaproject/)() const | Ottiene o imposta un [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Ottiene il numero di versioni del documento che è stato memorizzato nel documento DOC. |
| [get_ViewOptions](./get_viewoptions/)() | Fornisce opzioni per controllare come il documento viene visualizzato in Microsoft Word. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Chiamato durante varie procedure di elaborazione del documento quando viene rilevato un problema che potrebbe causare perdita di fedeltà dei dati o della formattazione. |
| [get_Watermark](./get_watermark/)() | Fornisce l'accesso al watermark del documento. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Restituisce una raccolta che rappresenta un elenco di componenti aggiuntivi del riquadro attività. |
| [get_WriteProtection](./get_writeprotection/)() | Fornisce l'accesso alle opzioni di protezione in scrittura del documento. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Ottiene le dimensioni della pagina, l'orientamento e altre informazioni su una pagina che potrebbero essere utili per la stampa o il rendering. |
| [GetText](../compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importa un nodo da un altro documento al documento corrente. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Unisce le sequenze con la stessa formattazione in tutti i paragrafi del documento. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Modifica i valori del tipo di campo [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) di [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) nell'intero documento affinché corrispondano ai tipi di campo contenuti nei codici di campo. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Protegge il documento dalle modifiche senza cambiare la password esistente o assegna una password casuale. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Protegge il documento dalle modifiche e opzionalmente imposta una password di protezione. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveBlankPages](./removeblankpages/)() | Rimuove le pagine vuote dal documento. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Rimuove le personalizzazioni della barra degli strumenti e dei comandi da tastiera dal documento. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Rimuove i riferimenti a schemi XML esterni da questo documento. |
| [RemoveMacros](./removemacros/)() | Rimuove tutte le macro (il progetto VBA) così come le barre degli strumenti e le personalizzazioni dei comandi dal documento. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Esegue il rendering di una pagina del documento in un oggetto **Graphics** a una scala specificata. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Esegue il rendering di una pagina del documento in un oggetto **Graphics** a una dimensione specificata. |
| [Save](./save/)(const System::String\&) | Salva il documento su un file. Determina automaticamente il formato di salvataggio dall'estensione. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Salva il documento su un file nel formato specificato. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Salva il documento in un file utilizzando le opzioni di salvataggio specificate. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Salva il documento in uno stream utilizzando il formato specificato. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Salva il documento in uno stream utilizzando le opzioni di salvataggio specificate. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../node/) che corrisponde all'espressione XPath. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Impostatore per [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Impostatore per [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Impostatore per [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Impostatore per [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Impostatore per [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostatore per [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Impostatore per [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Impostatore per [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Impostatore per [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Impostatore per [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Impostatore per [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Impostatore per [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Impostatore per [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Impostatore per [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Impostatore per [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Consente di controllare come vengono caricate le risorse esterne. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Impostatore per [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Impostatore per [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Impostatore per [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Impostatore per [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Impostatore per [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Impostatore per [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Impostatore per [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Impostatore per [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Inizia a contrassegnare automaticamente tutte le modifiche successive che apporti al documento programmaticamente come modifiche di revisione. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Inizia a contrassegnare automaticamente tutte le modifiche successive che apporti al documento programmaticamente come modifiche di revisione. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Interrompe il contrassegno automatico delle modifiche al documento come revisioni. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Scollega i campi in tutto il documento. |
| [Unprotect](./unprotect/)() | Rimuove la protezione dal documento indipendentemente dalla password. |
| [Unprotect](./unprotect/)(const System::String\&) | Rimuove la protezione dal documento se viene specificata una password corretta. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Aggiorna la proprietà [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) di tutte le note a piè di pagina e di chiusura nel documento. |
| [UpdateFields](./updatefields/)() | Aggiorna i valori dei campi in tutto il documento. |
| [UpdateListLabels](./updatelistlabels/)() | Aggiorna le etichette delle liste per tutti gli elementi di elenco nel documento. |
| [UpdatePageLayout](./updatepagelayout/)() | Ricostruisce il layout di pagina del documento. |
| [UpdateTableLayout](./updatetablelayout/)() | Implementa un approccio precedente al ricalcolo delle larghezze delle colonne della tabella che presenta problemi noti. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Aggiorna la [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento secondo le opzioni specificate. |
| [UpdateThumbnail](./updatethumbnail/)() | Aggiorna la [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento usando le opzioni predefinite. |
| [UpdateWordCount](./updatewordcount/)() | Aggiorna le proprietà del conteggio parole del documento. |
| [UpdateWordCount](./updatewordcount/)(bool) | Aggiorna le proprietà del conteggio parole del documento, opzionalmente aggiorna la proprietà [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/). |
## Note


Il [Document](./) è un oggetto centrale nella libreria Aspose.Words.

Per caricare un documento esistente in uno dei formati [LoadFormat](../loadformat/), passa un nome file o uno stream in uno dei costruttori di [Document](./). Per creare un documento vuoto, chiama il costruttore senza parametri.

Usa una delle sovraccariche del metodo Save per salvare il documento in uno dei formati [SaveFormat](../saveformat/).

Per disegnare le pagine del documento direttamente su un oggetto **Graphics** usa il metodo [RenderToScale()](../) o [RenderToSize()](../).

Per stampare il documento, usa uno dei metodi [Print()](../).

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

Il [Document](./) è un nodo radice di un albero che contiene tutti gli altri nodi del documento. L'albero è un pattern di progettazione Composite e in molti modi simile a XmlDocument. Il contenuto del documento può essere manipolato liberamente in modo programmatico:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Considera l'uso di [DocumentBuilder](../documentbuilder/) che semplifica il compito di creare o popolare programmaticamente l'albero del documento.

Il [Document](./) può contenere solo oggetti [Section](../section/).

In Microsoft Word, un documento valido deve contenere almeno una sezione.
## Vedi anche

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
