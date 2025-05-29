---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.MailMergeSettings per semplificare l'automazione dei documenti con potenti funzionalità di unione della stampa per una maggiore efficienza.
type: docs
weight: 6680
url: /it/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Specifica tutte le informazioni di unione di posta per un documento.

Per saperne di più, visita il[Unione di posta e creazione di report](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class MailMergeSettings
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Specifica l'indice a base uno del record dell'origine dati che verrà visualizzato in Microsoft Word. Il valore predefinito è 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Specifica la colonna all'interno dell'origine dati che contiene gli indirizzi e-mail. Il valore predefinito è una stringa vuota. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Specifica il tipo di segnalazione degli errori che deve essere effettuata da Microsoft Word quando si esegue una stampa unione. Il valore predefinito èDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Specifica la stringa di connessione utilizzata per connettersi a un'origine dati esterna. Il valore predefinito è una stringa vuota. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Specifica il percorso dell'origine dati per la stampa unione. Il valore predefinito è una stringa vuota. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Specifica il tipo di origine dati per la stampa unione e il metodo di accesso ai dati. Il valore predefinito èDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Specifica come Microsoft Word emetterà i risultati di una stampa unione. Il valore predefinito èDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. Il valore predefinito è`falso` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Specifica il percorso alla sorgente dell'intestazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Non sono sicuro di questo. Il riferimento all'automazione di Microsoft Word suggerisce che questo specifichi che la query venga eseguita ogni volta che il documento viene aperto in Microsoft Word. Tuttavia, la specifica OOXML suggerisce che questo specifichi che la query contiene un riferimento a un file di query esterno che contiene la query stessa. Il valore predefinito è`falso` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e-mail come allegati anziché come corpo dell'e-mail stessa. Il valore predefinito è`falso` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Specifica il testo che deve apparire nella riga dell'oggetto delle e-mail o dei fax prodotti durante la stampa unione. Il valore predefinito è una stringa vuota. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Specifica il tipo di documento principale della stampa unione. Il valore predefinito èDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Ottiene o imposta l'oggetto che specifica le impostazioni dell'Office Data Source Object (ODSO). |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Contiene la stringa del linguaggio di query strutturato che deve essere eseguita sulla sorgente dati esterna specificata per restituire il set di record che deve essere importato nel documento quando viene eseguita l'operazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata in cui sono stati inseriti i campi di unione (ad esempio, visualizzare in anteprima i dati uniti). Il valore predefinito è`falso` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Cancella le impostazioni di stampa unione in modo che quando il documento viene salvato, nessuna impostazione di stampa unione verrà salvata e diventerà un documento normale. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Restituisce un clone profondo di questo oggetto. |

## Osservazioni

È possibile utilizzare questo oggetto per specificare un'origine dati per la stampa unione per un documento e queste informazioni (insieme ai campi dati disponibili) verranno visualizzate in Microsoft Word quando l'utente apre il documento. In alternativa, è possibile utilizzare questo oggetto per interrogare le impostazioni per la stampa unione specificate dall'utente in Microsoft Word per questo documento.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni di unione posta di un documento sono sempre disponibili tramite[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) proprietà.

Per rilevare se questo documento è un documento principale di stampa unione, controllare il valore di [`MainDocumentType`](./maindocumenttype/) proprietà.

Per rimuovere le impostazioni di unione di posta e le informazioni sull'origine dati da un documento, è possibile utilizzare [`Clear`](./clear/) metodo. Aspose.Words non scriverà le impostazioni di unione di posta in un documento se il[`MainDocumentType`](./maindocumenttype/) la proprietà è impostata suNotAMergeDocument o il[`DataType`](./datatype/) la proprietà è impostata suNone.

Il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare manualmente un documento con una sorgente dati desiderata in Microsoft Word e quindi aprire tale documento utilizzando Aspose.Words ed esaminare le proprietà dell'[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) E[`Odso`](./odso/) oggetti. Questo è sicuramente un buon approccio da adottare se si desidera imparare a configurare a livello di programmazione un'origine dati, ad esempio.

Aspose.Words conserva le informazioni di unione di posta durante il caricamento, il salvataggio e la conversione di documenti tra formati diversi, ma non utilizza queste informazioni quando esegue la propria unione di posta utilizzando[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) oggetto.

## Esempi

Mostra come eseguire una stampa unione con dati provenienti da un oggetto origine dati di Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Crea una sorgente dati sotto forma di file ASCII, con il carattere "|"
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

 // L'apertura di questo documento in Microsoft Word eseguirà la stampa unione prima di visualizzarne il contenuto.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
