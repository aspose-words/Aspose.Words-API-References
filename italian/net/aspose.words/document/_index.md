---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words per .NET
description: Aspose.Words.Document classe. Rappresenta un documento Word in C#.
type: docs
weight: 430
url: /it/net/aspose.words/document/
---
## Document class

Rappresenta un documento Word.

Per saperne di più, visita il[Lavorare con il documento](https://docs.aspose.com/words/net/working-with-document/) articolo di documentazione.

```csharp
public class Document : DocumentBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Document](document/#constructor)() | Crea un documento Word vuoto. |
| [Document](document/#constructor_1)(*Stream*) | Apre un documento esistente da uno stream. Rileva automaticamente il formato del file. |
| [Document](document/#constructor_3)(*string*) | Apre un documento esistente da un file. Rileva automaticamente il formato del file. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Apre un documento esistente da uno stream. Consente di specificare opzioni aggiuntive come una password di crittografia. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Apre un documento esistente da un file. Consente di specificare opzioni aggiuntive come una password di crittografia. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Ottiene o imposta il percorso completo del modello allegato al documento. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Ottiene o imposta un flag che indica se gli stili nel documento vengono aggiornati per corrispondere agli stili nel modello allegato ogni volta che il documento viene aperto in MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Ottiene o imposta la forma dello sfondo del documento. Può essere`nullo` . |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Restituisce una raccolta che rappresenta tutte le proprietà del documento integrate nel documento. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Fornisce l'accesso alle opzioni di compatibilità del documento (ovvero, le preferenze dell'utente immesse nel file**Compatibilità** scheda del**Opzioni** finestra di dialogo in Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Ottiene la versione di conformità OOXML determinata dal contenuto del documento caricato. Ha senso solo per i documenti OOXML. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Restituisce una raccolta che rappresenta tutte le proprietà del documento personalizzato del documento. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Ottiene o imposta la raccolta di parti di archiviazione dati XML personalizzate. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Ottiene o imposta l'intervallo (in punti) tra le tabulazioni predefinite. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Ottiene la raccolta di firme digitali per questo documento e i relativi risultati di convalida. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Ottiene questa istanza. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Fornisce opzioni che controllano la numerazione e il posizionamento delle note di chiusura in questo documento. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Ottiene a[`FieldOptions`](../../aspose.words.fields/fieldoptions/) oggetto che rappresenta le opzioni per controllare la gestione dei campi nel documento. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Ottiene la prima sezione del documento. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Ottiene o imposta le impostazioni dei caratteri del documento. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questo documento. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Restituisce a[`Frameset`](./frameset/)esempio se questo documento rappresenta una pagina con frame. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Ottiene o imposta il documento di glossario all'interno di questo documento o modello. Un documento di glossario è un archivio per le voci di glossario, correzione automatica e Building Block definite in un documento. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Restituisce`VERO` se è stata effettuata la verifica grammaticale del documento. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Restituisce`VERO` se il documento ha un progetto VBA (macro). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Restituisce`VERO` se il documento contiene modifiche rilevate. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Fornisce l'accesso alle opzioni di sillabazione del documento. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Specifica se includere caselle di testo, note a piè di pagina e note di chiusura nelle statistiche sul conteggio delle parole. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Ottiene l'ultima sezione del documento. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Ottiene a[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) oggetto che rappresenta le opzioni per controllare il processo di layout di questo documento. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Fornisce l'accesso alla formattazione dell'elenco utilizzata nel documento. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Restituisce a[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) oggetto che rappresenta la funzionalità di stampa unione per il documento. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Ottiene o imposta l'oggetto che contiene tutte le informazioni sulla stampa unione per un documento. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | RestituisceDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Ottiene il nome del file originale del documento. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Ottiene il formato del documento originale caricato in questo oggetto. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Ottiene o imposta la raccolta di parti personalizzate (contenuto arbitrario) collegate al pacchetto OOXML utilizzando "relazioni sconosciute". |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione più semplice di[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Ottiene il numero di pagine nel documento calcolato dall'operazione di impaginazione più recente. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Ottiene il tipo di protezione del documento attualmente attivo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Ottiene o imposta un flag che indica che Microsoft Word rimuoverà tutte le informazioni dell'utente da commenti, revisioni e proprietà del documento al momento del salvataggio del documento. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permette di controllare come vengono caricate le risorse esterne. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Ottiene una raccolta di revisioni (modifiche rilevate) presenti in questo documento. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Ottiene o imposta un valore che indica se lavorare con la versione originale o rivista di un documento. |
| [Sections](../../aspose.words/document/sections/) { get; } | Restituisce una raccolta che rappresenta tutte le sezioni del documento. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Specifica se attivare l'ombreggiatura grigia sui campi del modulo. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Specifica se visualizzare gli errori grammaticali in questo documento. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Specifica se visualizzare gli errori di ortografia in questo documento. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Restituisce`VERO` se il documento è stato controllato dall'ortografia. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Restituisce una raccolta di stili definiti nel documento. |
| [Theme](../../aspose.words/document/theme/) { get; } | Ottiene il file[`Theme`](./theme/) oggetto per questo documento. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | Vero se le modifiche vengono tracciate quando il documento viene modificato in Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Restituisce la raccolta di variabili aggiunte a un documento o modello. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Ottiene o imposta a[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Ottiene il numero di versioni del documento archiviate nel documento DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Fornisce opzioni per controllare la modalità di visualizzazione del documento in Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Fornisce l'accesso alla filigrana del documento. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Restituisce una raccolta che rappresenta un elenco di componenti aggiuntivi del riquadro attività. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Fornisce l'accesso alle opzioni di protezione da scrittura del documento. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Accetta tutte le modifiche tracciate nel documento. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi secondari per questo nodo. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Aggiunge il documento specificato alla fine di questo documento. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Aggiunge il documento specificato alla fine di questo documento. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Pulisce gli stili e gli elenchi inutilizzati dal documento. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Pulisce gli stili e gli elenchi inutilizzati dal documento in base a quanto specificato[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Esegue una copia approfondita del file`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Confronta questo documento con un altro documento producendo modifiche come numero di modifiche e revisioni del formato[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Confronta questo documento con un altro documento producendo modifiche come una serie di modifiche e revisioni del formato[`Revision`](../revision/) . Permette di specificare le opzioni di confronto utilizzando[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Copia gli stili dal modello specificato in un documento. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Copia gli stili dal modello specificato in un documento. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Se il documento non contiene sezioni, crea una sezione con un paragrafo. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Converte la formattazione specificata negli stili di tabella in formattazione diretta sulle tabelle del documento. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | Restituisce il`Document` oggetto che rappresenta l'intervallo di pagine specificato. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Ottiene le dimensioni della pagina, l'orientamento e altre informazioni su una pagina che potrebbero essere utili per la stampa o il rendering. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Importa un nodo da un altro documento al documento corrente. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Restituisce l'indice del nodo figlio specificato nell'array di nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Inserisce il nodo specificato immediatamente dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | I join vengono eseguiti con la stessa formattazione in tutti i paragrafi del documento. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Modifica i valori del tipo di campo[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) Di[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) nell'intero documento in modo che corrispondano ai tipi di campo contenuti nei codici di campo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi secondari per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Print](../../aspose.words/document/print/#print)() | Stampa l'intero documento sulla stampante predefinita. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Stampa il documento in base alle impostazioni della stampante specificate, utilizzando il controller di stampa standard (senza interfaccia utente). |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Stampa l'intero documento sulla stampante specificata, utilizzando il controller di stampa standard (senza interfaccia utente). |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Stampa il documento in base alle impostazioni della stampante specificate, utilizzando il controller di stampa standard (senza interfaccia utente) e un nome documento. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Protegge il documento da modifiche senza cambiare la password esistente o assegna una password casuale. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Protegge il documento dalle modifiche e facoltativamente imposta una password di protezione. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Rimuove il nodo figlio specificato. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Rimuove i riferimenti allo schema XML esterno da questo documento. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Rimuove tutte le macro (il progetto VBA), nonché le barre degli strumenti e le personalizzazioni dei comandi dal documento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Rende una pagina del documento in un fileGraphics oggetto su una scala specificata. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Rende una pagina del documento in un fileGraphics oggetto a una dimensione specificata. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Salva il documento in un file. Determina automaticamente il formato di salvataggio dall'estensione. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Salva il documento in un flusso utilizzando il formato specificato. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Salva il documento in uno stream utilizzando le opzioni di salvataggio specificate. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Salva il documento in un file nel formato specificato. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Salva il documento in un file utilizzando le opzioni di salvataggio specificate. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Invia il documento al browser client. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Inizia a contrassegnare automaticamente tutte le ulteriori modifiche apportate al documento a livello di codice come modifiche di revisione. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Inizia a contrassegnare automaticamente tutte le ulteriori modifiche apportate al documento a livello di codice come modifiche di revisione. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Interrompe il contrassegno automatico delle modifiche al documento come revisioni. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Scollega i campi dell'intero documento. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Rimuove la protezione dal documento indipendentemente dalla password. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Rimuove la protezione dal documento se viene specificata una password corretta. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Aggiorna i valori dei campi nell'intero documento. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Aggiorna le etichette dell'elenco per tutti gli elementi dell'elenco nel documento. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Ricostruisce l'impaginazione del documento. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Aggiornamenti[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento utilizzando le opzioni predefinite. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Aggiornamenti[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento secondo le opzioni specificate. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Aggiorna le proprietà del conteggio delle parole del documento. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Aggiorna le proprietà del conteggio delle parole del documento, facoltativamente aggiornamenti[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) proprietà. |

## Osservazioni

IL`Document` è un oggetto centrale nella libreria Aspose.Words.

Per caricare un documento esistente in uno qualsiasi dei file[`LoadFormat`](../loadformat/) formati, passare un nome file o uno stream in uno dei formati`Document`costruttori. Per creare un documento vuoto, chiama il costruttore senza parametri.

Utilizza uno degli overload del metodo Save per salvare il documento in uno qualsiasi dei [`SaveFormat`](../saveformat/) formati.

Per disegnare le pagine del documento direttamente su a**Grafica** oggetto use [`RenderToScale`](./rendertoscale/) O[`RenderToSize`](./rendertosize/) metodo.

Per stampare il documento, utilizzare uno dei file[`Print`](./print/) metodi.

[`MailMerge`](./mailmerge/) è il motore di reporting di Aspose.Words che consente di popolare report progettati in Microsoft Word con dati provenienti da varie origini dati in modo rapido e semplice. I dati possono provenire da un DataSet, DataTable, DataView, IDataReader o un array di valori. **Stampa unione** esaminerà i record trovati nell'origine dati e li inserirà nei campi di stampa unione del documento ampliandoli secondo necessità.

`Document` memorizza informazioni a livello di documento come[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) elenchi e macro. La maggior parte di questi oggetti sono accessibili tramite le proprietà corrispondenti del`Document`.

IL`Document` è un nodo radice di un albero che contiene tutti gli altri nodi del documento. L'albero è un modello di progettazione composito e per molti versi simile a XmlDocument. Il contenuto del documento può essere manipolato liberamente a livello di programmazione:

* È possibile accedere ai nodi del documento tramite raccolte tipizzate, ad esempio[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) eccetera.
* I nodi del documento possono essere selezionati in base al tipo di nodo utilizzando [`GetChildNodes`](../compositenode/getchildnodes/) o utilizzando una query XPath con[`SelectNodes`](../compositenode/selectnodes/) O[`SelectSingleNode`](../compositenode/selectsinglenode/).
* I nodi di contenuto possono essere aggiunti o rimossi da qualsiasi punto del documento utilizzando [`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) e altri metodi forniti dalla classe base[`CompositeNode`](../compositenode/).
* Gli attributi di formattazione di ciascun nodo possono essere modificati tramite le proprietà di quel nodo.

Considera l'utilizzo[`DocumentBuilder`](../documentbuilder/)che semplifica l'attività di creazione o di popolamento dell'albero del documento a livello di codice.

IL`Document` può contenere solo[`Section`](../section/) oggetti.

In Microsoft Word, un documento valido deve avere almeno una sezione.

## Esempi

Mostra come eseguire una stampa unione con i dati di un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione di output per ogni riga nella tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizza una riga della tabella per creare un documento di stampa unione di output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento di origine per la stampa unione.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Guarda anche

* class [DocumentBase](../documentbase/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
