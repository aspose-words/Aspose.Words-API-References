---
title: MailMergeDestination
second_title: Aspose.Words per .NET API Reference
description: Specifica i possibili risultati che possono essere generati quando viene eseguita una stampa unione su un documento.
type: docs
weight: 5530
url: /it/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Specifica i possibili risultati che possono essere generati quando viene eseguita una stampa unione su un documento.

```csharp
public enum MailMergeDestination
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| NewDocument | `0` | Specifica che le applicazioni di hosting conformi generano nuovi documenti popolando i campi all'interno di un determinato documento con i dati dell'origine dati esterna specificata. |
| Printer | `1` | Specifica che le applicazioni di hosting conformi devono stampare i documenti risultanti dalla compilazione dei campi all'interno di un determinato documento con dati esterni dall'origine dati esterna specificata. |
| Email | `2` | Specifica che le applicazioni di hosting conformi devono generare e-mail utilizzando i documenti risultanti da popolando i campi all'interno di un determinato documento con i dati dell'origine dati esterna specificata. |
| Fax | `4` | Specifica che le applicazioni di hosting conformi devono generare fax utilizzando i documenti risultanti da popolando i campi all'interno di un determinato documento con i dati dell'origine dati esterna specificata. |
| Default | `0` | Uguale aNewDocument valore. |

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

* property [Destination](../mailmergesettings/destination)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->