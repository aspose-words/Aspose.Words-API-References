---
title: RtfLoadOptions
second_title: Aspose.Words per .NET API Reference
description: Consente di specificare opzioni aggiuntive durante il caricamentoRtf documento in aDocument../aspose.words/document oggetto.
type: docs
weight: 3510
url: /it/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamentoRtf documento in a[`Document`](../../aspose.words/document) oggetto.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions)() | Inizializza una nuova istanza di questa classe con valori predefiniti. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere una stringa nulla o vuota. Il valore predefinito è null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Ottiene o imposta se convertire il metafile (Wmf oEmf ) immagini aPng formato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | Ottiene o imposta se convertire forme con EquationXML in oggetti Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere nullo. Il valore predefinito è null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Consente di specificare le impostazioni del carattere del documento. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Ottiene le preferenze della lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una specifica versione di MS Word. Il valore predefinito èWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere una stringa nulla o vuota. Il valore predefinito è null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Ottiene o imposta se mantenere il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Chiamato durante il caricamento di un documento e accetta i dati sull'avanzamento del caricamento. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text) { get; set; } | Quando è impostato su vero,CharsetDetectorcercherà di rilevare i caratteri UTF8, verranno conservati durante l'importazione. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Consente di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione. |

### Esempi

Mostra come rilevare i caratteri UTF-8 durante il caricamento di un documento RTF.

```csharp
// Crea un oggetto "RtfLoadOptions" per modificare il modo in cui carichiamo un documento RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Imposta la proprietà "RecognizeUtf8Text" su "false" per presumere che il documento utilizzi il set di caratteri ISO 8859-1
// e carica tutti i caratteri nel documento.
// Imposta la proprietà "RecognizeUtf8Text" su "true" per analizzare tutti i caratteri di lunghezza variabile che possono essere presenti nel testo.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Guarda anche

* class [LoadOptions](../loadoptions)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
