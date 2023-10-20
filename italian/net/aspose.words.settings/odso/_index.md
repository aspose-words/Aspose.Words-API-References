---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words per .NET
description: Aspose.Words.Settings.Odso classe. Specifica le impostazioni ODSO Office Data Source Object per unorigine dati di stampa unione in C#.
type: docs
weight: 5880
url: /it/net/aspose.words.settings/odso/
---
## Odso class

Specifica le impostazioni ODSO (Office Data Source Object) per un'origine dati di stampa unione.

Per saperne di più, visita il[Stampa unione e reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

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
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Specifica il carattere che deve essere interpretato come delimitatore di colonna utilizzato per separare le colonne all'interno di origini dati esterne. Il valore predefinito è 0, il che significa che non è definito alcun delimitatore di colonna. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Specifica il percorso dell'origine dati esterna da connettere a un documento per eseguire la stampa unione. Il valore predefinito è una stringa vuota. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Specifica il tipo di origine dati esterna a cui connettersi come parte delle informazioni di connessione ODSO per questa stampa unione. Il valore predefinito èDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Ottiene o imposta una raccolta di oggetti che specificano il modo in cui le colonne dell'origine dati esterna vengono mappate ai nomi dei campi di unione predefiniti nel documento. Questo oggetto non viene mai`nullo` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Specifica che un'applicazione hosting tratterà la prima riga di dati nell'origine dati esterna specificata come una riga di intestazione contenente i nomi di ciascuna colonna nell'origine dati. Il valore predefinito è`falso` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Ottiene o imposta una raccolta di oggetti che specificano l'inclusione/esclusione di singoli record nella stampa unione. Questo oggetto non viene mai`nullo` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Specifica il particolare set di dati a cui deve essere connessa un'origine all'interno di un'origine dati esterna. Il valore predefinito è una stringa vuota. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per connettersi a un'origine dati esterna. Il valore predefinito è una stringa vuota. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Restituisce un clone profondo di questo oggetto. |

## Osservazioni

ODSO sembra essere il "nuovo" modo in cui le versioni più recenti di Microsoft Word preferiscono utilizzare quando specificano determinati tipi di origini dati per un documento di stampa unione. ODSO probabilmente è apparso per la prima volta in Microsoft Word 2000.

L'uso di ODSO è scarsamente documentato e il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare manualmente un documento con l'origine dati desiderata in Microsoft Word e quindi aprire quel documento utilizzando Aspose.Words ed esaminare le proprietà del[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) e [`Odso`](../mailmergesettings/odso/)oggetti. Questo è un buon approccio da adottare se vuoi imparare come configurare a livello di codice un'origine dati, ad esempio.

Normalmente non è necessario creare direttamente gli oggetti di questa classe poiché le impostazioni ODSO sono sempre disponibili tramite[`Odso`](../mailmergesettings/odso/) proprietà.

## Esempi

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

 // L'apertura di questo documento in Microsoft Word eseguirà la stampa unione prima di visualizzarne il contenuto.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
