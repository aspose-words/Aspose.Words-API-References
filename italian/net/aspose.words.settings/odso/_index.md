---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Settings.Odso per un'integrazione perfetta con la stampa unione. Ottimizza le impostazioni ODSO per una gestione efficiente delle fonti dati.
type: docs
weight: 6710
url: /it/net/aspose.words.settings/odso/
---
## Odso class

Specifica le impostazioni ODSO (Office Data Source Object) per un'origine dati di stampa unione.

Per saperne di più, visita il[Unione di posta e creazione di report](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class Odso
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Odso](odso/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Specifica il carattere che deve essere interpretato come delimitatore di colonna utilizzato per separare le colonne all'interno di origini dati esterne. Il valore predefinito è 0, il che significa che non è stato definito alcun delimitatore di colonna. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Specifica la posizione dell'origine dati esterna da connettere a un documento per eseguire la stampa unione. Il valore predefinito è una stringa vuota. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Specifica il tipo di origine dati esterna a cui connettersi come parte delle informazioni di connessione ODSO per questa unione di stampa. Il valore predefinito èDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Ottiene o imposta una raccolta di oggetti che specificano come le colonne dell'origine dati esterna vengono mappate ai nomi dei campi di unione predefiniti nel documento. Questo oggetto non è mai`null` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Specifica che un'applicazione di hosting deve trattare la prima riga di dati nella sorgente dati esterna specificata come una riga di intestazione contenente i nomi di ciascuna colonna nella sorgente dati. Il valore predefinito è`falso` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Ottiene o imposta una raccolta di oggetti che specificano l'inclusione/esclusione di singoli record nella stampa unione. Questo oggetto non è mai`null` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Specifica il set di dati specifico a cui un'origine deve essere connessa all'interno di un'origine dati esterna. Il valore predefinito è una stringa vuota. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per connettersi a un'origine dati esterna. Il valore predefinito è una stringa vuota. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Restituisce un clone profondo di questo oggetto. |

## Osservazioni

ODSO sembra essere il "nuovo" metodo che le versioni più recenti di Microsoft Word preferiscono utilizzare quando specificano determinati tipi di origini dati per un documento di stampa unione. ODSO è probabilmente apparso per la prima volta in Microsoft Word 2000.

L'uso di ODSO è scarsamente documentato e il modo migliore per imparare a usare le proprietà di questo oggetto è creare manualmente un documento con una fonte dati desiderata in Microsoft Word e quindi aprire quel documento usando Aspose.Words ed esaminare le proprietà del[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) e [`Odso`](../mailmergesettings/odso/)oggetti. Questo è un buon approccio da adottare se si desidera imparare come configurare a livello di codice una sorgente dati, ad esempio.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni ODSO sono sempre disponibili tramite[`Odso`](../mailmergesettings/odso/) proprietà.

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
