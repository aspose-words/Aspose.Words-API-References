---
title: MailMergeSettings
second_title: Aspose.Words per .NET API Reference
description: Specifica tutte le informazioni sulla stampa unione per un documento.
type: docs
weight: 5550
url: /it/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Specifica tutte le informazioni sulla stampa unione per un documento.

```csharp
public class MailMergeSettings
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MailMergeSettings](mailmergesettings)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord) { get; set; } | Specifica l'indice a base uno del record dall'origine dati che verrà visualizzato in Microsoft Word. Il valore predefinito è 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname) { get; set; } | Specifica la colonna all'interno dell'origine dati che contiene gli indirizzi di posta elettronica. Il valore predefinito è una stringa vuota. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors) { get; set; } | Specifica il tipo di segnalazione degli errori che deve essere eseguita da Microsoft Word durante l'esecuzione di una stampa unione. Il valore predefinito èDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring) { get; set; } | Specifica la stringa di connessione utilizzata per connettersi a un'origine dati esterna. Il valore predefinito è una stringa vuota. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource) { get; set; } | Specifica il percorso dell'origine dati di stampa unione. Il valore predefinito è una stringa vuota. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype) { get; set; } | Specifica il tipo di origine dati per la stampa unione e il metodo di accesso ai dati. Il valore predefinito èDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination) { get; set; } | Specifica come Microsoft Word produrrà i risultati di una stampa unione. Il valore predefinito èDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines) { get; set; } | Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. Il valore predefinito è`falso` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource) { get; set; } | Specifica il percorso dell'origine dell'intestazione della stampa unione. Il valore predefinito è una stringa vuota. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery) { get; set; } | Non sono sicuro di questo. Il riferimento di automazione di Microsoft Word suggerisce che questo specifica che la query viene eseguita ogni volta che il documento viene aperto in Microsoft Word. Ma la specifica OOXML suggerisce che questo specifichi che la query contiene un riferimento a un file di query esterno che contiene la query effettiva. Il valore predefinito è`falso` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment) { get; set; } | Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati tramite e-mail come allegato anziché rispetto al corpo dell'e-mail effettiva. Il valore predefinito è`falso` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject) { get; set; } | Specifica il testo che deve apparire nella riga dell'oggetto delle e-mail o dei fax prodotti durante la stampa unione. Il valore predefinito è una stringa vuota. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype) { get; set; } | Specifica il tipo di documento principale della stampa unione. Il valore predefinito èDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso) { get; set; } | Ottiene o imposta l'oggetto che specifica le impostazioni ODSO (Office Data Source Object). |
| [Query](../../aspose.words.settings/mailmergesettings/query) { get; set; } | Contiene la stringa Structured Query Language che deve essere eseguita sull'origine dati esterna specificata per restituire la serie di record che devono essere importati nel documento quando viene eseguita l'operazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata) { get; set; } | Specifica che Microsoft Word visualizzerà i dati dall'origine dati esterna specificata in cui sono stati inseriti i campi di unione (es. anteprima dei dati uniti). Il valore predefinito è`falso` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear)() | Cancella le impostazioni della stampa unione in modo tale che quando il documento viene salvato, non verrà salvata alcuna impostazione della stampa unione e diventerà un documento normale. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone)() | Restituisce un clone profondo di questo oggetto. |

### Osservazioni

È possibile utilizzare questo oggetto per specificare un'origine dati per la stampa unione per un documento e queste informazioni (insieme ai campi dati disponibili) verranno visualizzate in Microsoft Word quando l'utente apre questo documento. Oppure è possibile utilizzare questo oggetto per interrogare le impostazioni della stampa unione che l'utente ha specificato in Microsoft Word per questo documento.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni di stampa unione di un documento sono sempre disponibili tramite il[`MailMergeSettings`](../../aspose.words/document/mailmergesettings) proprietà.

Per rilevare se questo documento è un documento principale di stampa unione, controlla il valore di [`MainDocumentType`](./maindocumenttype) proprietà.

Per rimuovere le impostazioni della stampa unione e le informazioni sull'origine dati da un documento, puoi utilizzare [`Clear`](./clear) metodo. Aspose.Words non scriverà le impostazioni di stampa unione in un documento se il[`MainDocumentType`](./maindocumenttype) la proprietà è impostata suNotAMergeDocument o il[`DataType`](./datatype) la proprietà è impostata suNone.

Il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare manualmente un documento con un'origine dati desiderata in Microsoft Word, quindi aprire quel documento utilizzando Aspose.Words ed esaminare le proprietà dell'oggetto[`MailMergeSettings`](../../aspose.words/document/mailmergesettings) e[`Odso`](./odso) oggetti. Questo è un buon approccio da adottare se si desidera imparare a configurare a livello di codice un'origine dati, ad esempio.

Aspose.Words conserva le informazioni sulla stampa unione durante il caricamento, il salvataggio e la conversione di documenti tra formati diversi, ma non utilizza queste informazioni quando si esegue la propria stampa unione utilizzando il[`MailMerge`](../../aspose.words.mailmerging/mailmerge) oggetto.

### Esempi

Mostra come eseguire una stampa unione con i dati di un oggetto origine dati di Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Crea un'origine dati sotto forma di file ASCII, con "|" carattere
// funge da delimitatore che separa le colonne. La prima riga contiene i nomi delle tre colonne,
// e ogni riga successiva è una riga con i rispettivi valori.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

// L'apertura di questo documento in Microsoft Word eseguirà la stampa unione prima di visualizzare il contenuto. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
