---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Loading.HtmlLoadOptions per migliorare il caricamento di documenti HTML in un oggetto Document con opzioni personalizzabili per prestazioni ottimali.
type: docs
weight: 4070
url: /it/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamento di un documento HTML in un[`Document`](../../aspose.words/document/) oggetto.

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Inizializza una nuova istanza di questa classe con valori predefiniti. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | Una scorciatoia per inizializzare una nuova istanza di questa classe con proprietà impostate sui valori specificati. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Ottiene o imposta un valore che specifica come vengono importate le proprietà degli elementi a livello di blocco. Il valore predefinito èMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire metafile(Wmf OEmf ) immagini aPngformato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Ottiene o imposta un valore che indica se convertire le immagini SVG caricate nel formato EMF. Il valore predefinito è`falso` e, se possibile, le immagini SVG caricate vengono memorizzate così come sono, senza conversione. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`null` Il valore predefinito è`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Consente di specificare le impostazioni del font del documento. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Ottiene o imposta un valore che indica se ignorare gli elementi HTML &lt;noscript&gt;. Il valore predefinito è `falso` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifica se ignorare i dati OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze di lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito èWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Ottiene o imposta il tipo preferito di nodi del documento che rappresenteranno gli elementi &lt;input&gt; e &lt;select&gt; importati. Il valore predefinito è FormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ottiene o imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Viene chiamato durante il caricamento di un documento e accetta dati sullo stato di avanzamento del caricamento. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Consente di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | Ottiene o imposta un valore che indica se supportare le regole @font-face e se caricare i font dichiarati. Il valore predefinito è `falso` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Ottiene o imposta un valore che indica se supportare le immagini VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ottiene o imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti di impostazione della pagina. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Numero di millisecondi di attesa prima che la richiesta web scada. Il valore predefinito è 100000 millisecondi (100 secondi). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |

## Esempi

Mostra come supportare i commenti condizionali durante il caricamento di un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Se il valore è true, prendiamo in considerazione il codice VML durante l'analisi del documento caricato.
loadOptions.SupportVml = supportVml;

// Questo documento contiene un'immagine JPEG tra i tag "<!--[if gte vml 1]>",
// e un'immagine PNG diversa all'interno dei tag "<![if !vml]>".
// Se impostiamo il flag "SupportVml" su "true", Aspose.Words caricherà il JPEG.
// Se impostiamo questo flag su "false", Aspose.Words caricherà solo il PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Guarda anche

* class [LoadOptions](../loadoptions/)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
