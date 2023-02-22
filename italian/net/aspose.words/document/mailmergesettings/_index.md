---
title: Document.MailMergeSettings
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene o imposta loggetto che contiene tutte le informazioni sulla stampa unione per un documento.
type: docs
weight: 250
url: /it/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Ottiene o imposta l'oggetto che contiene tutte le informazioni sulla stampa unione per un documento.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

### Osservazioni

È possibile utilizzare questo oggetto per specificare un'origine dati per la stampa unione per un documento e queste informazioni (insieme ai campi dati disponibili) verranno visualizzate in Microsoft Word quando l'utente apre questo documento. Oppure è possibile utilizzare questo oggetto per interrogare le impostazioni della stampa unione che l'utente ha specificato in Microsoft Word per questo documento.

Questo oggetto non è mai nullo.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


