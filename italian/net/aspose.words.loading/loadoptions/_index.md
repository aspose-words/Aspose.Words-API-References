---
title: Class LoadOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Loading.LoadOptions classe. Permette di specificare opzioni aggiuntive come password o URI di base quando si carica un documento in unDocument oggetto.
type: docs
weight: 3660
url: /it/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Permette di specificare opzioni aggiuntive (come password o URI di base) quando si carica un documento in un[`Document`](../../aspose.words/document/) oggetto.

Per saperne di più, visita il[Specificare le opzioni di caricamento](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public class LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Inizializza una nuova istanza di questa classe con valori predefiniti. |
| [LoadOptions](loadoptions/#constructor_2)(string) | Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate sui valori specificati. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`nullo` o stringa vuota. L'impostazione predefinita è`nullo` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire il metafile (Wmf OEmf ) immagini aPng formato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`nullo` . L'impostazione predefinita è`nullo` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permette di specificare le impostazioni dei caratteri del documento. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifica se ignorare i dati OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze della lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permette di specificare che il processo di caricamento del documento deve corrispondere a una specifica versione di MS Word. Il valore predefinito èWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`nullo` o stringa vuota. L'impostazione predefinita è`nullo` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ottiene o imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Chiamato durante il caricamento di un documento e accetta i dati sull'avanzamento del caricamento. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permette di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permette di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### Esempi

Mostra come caricare un documento Microsoft Word crittografato.

```csharp
Document doc;

// Aspose.Words lancia un'eccezione se proviamo ad aprire un documento crittografato senza la sua password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Quando si carica un documento di questo tipo, la password viene passata al costruttore del documento utilizzando un oggetto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Esistono due modi per caricare un documento crittografato con un oggetto LoadOptions.
// 1 - Carica il documento dal file system locale in base al nome file:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Carica il documento da uno stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)


