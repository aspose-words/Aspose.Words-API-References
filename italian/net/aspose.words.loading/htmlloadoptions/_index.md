---
title: Class HtmlLoadOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Loading.HtmlLoadOptions classe. Consente di specificare opzioni aggiuntive durante il caricamento di un documento HTML in un fileDocument oggetto.
type: docs
weight: 3420
url: /it/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamento di un documento HTML in un file[`Document`](../../aspose.words/document/) oggetto.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Inizializza una nuova istanza di questa classe con valori predefiniti. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | Un collegamento per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | Un collegamento per inizializzare una nuova istanza di questa classe con le proprietà impostate sui valori specificati. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere una stringa nulla o vuota. Il valore predefinito è null. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Ottiene o imposta un valore che specifica come vengono importate le proprietà degli elementi a livello di blocco. Il valore predefinito èMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire il metafile (Wmf oEmf ) immagini aPng formato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire forme con EquationXML in oggetti Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Ottiene o imposta un valore che indica se convertire le immagini SVG caricate nel formato EMF. Il valore predefinito è`falso` e, se possibile, le immagini SVG caricate vengono archiviate così come sono senza conversione. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere nullo. Il valore predefinito è null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Consente di specificare le impostazioni del carattere del documento. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Ottiene o imposta un valore che indica se ignorare gli elementi HTML &lt;noscript&gt;. Il valore predefinito è`falso` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze della lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una specifica versione di MS Word. Il valore predefinito èWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere una stringa nulla o vuota. Il valore predefinito è null. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Ottiene o imposta il tipo preferito di nodi del documento che rappresenteranno gli elementi &lt;input&gt; e &lt;select&gt; importati. Il valore predefinito èFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ottiene o imposta se mantenere il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Chiamato durante il caricamento di un documento e accetta i dati sull'avanzamento del caricamento. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Consente di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Ottiene o imposta un valore che indica se supportare le immagini VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Il numero di millisecondi di attesa prima del timeout della richiesta Web. Il valore predefinito è 100000 millisecondi (100 secondi). |

### Guarda anche

* class [LoadOptions](../loadoptions/)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)


