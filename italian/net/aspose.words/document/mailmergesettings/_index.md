---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà MailMergeSettings per gestire in modo efficiente tutti i dati di stampa unione del tuo documento e migliorare il flusso di lavoro.
type: docs
weight: 280
url: /it/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Ottiene o imposta l'oggetto che contiene tutte le informazioni di unione di stampa per un documento.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## Osservazioni

È possibile utilizzare questo oggetto per specificare un'origine dati per la stampa unione per un documento e queste informazioni (insieme ai campi dati disponibili) verranno visualizzate in Microsoft Word quando l'utente apre il documento. In alternativa, è possibile utilizzare questo oggetto per interrogare le impostazioni per la stampa unione specificate dall'utente in Microsoft Word per questo documento.

Questo oggetto non è mai`null`.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
