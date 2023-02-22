---
title: Enum MailMergeCheckErrors
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Settings.MailMergeCheckErrors enum. Specifica come Microsoft Word riporterà gli errori rilevati durante la stampa unione.
type: docs
weight: 5510
url: /it/net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

Specifica come Microsoft Word riporterà gli errori rilevati durante la stampa unione.

```csharp
public enum MailMergeCheckErrors
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Simulate | `1` | Simula l'unione e segnala gli errori in un nuovo documento. |
| PauseOnError | `2` | Completa l'unione e metti in pausa per segnalare gli errori. |
| CollectErrors | `3` | Completa l'unione e segnala gli errori in un nuovo documento. |
| Default | `2` | Uguale aPauseOnError valore. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)


