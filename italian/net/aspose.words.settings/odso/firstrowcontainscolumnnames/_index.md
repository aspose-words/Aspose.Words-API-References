---
title: Odso.FirstRowContainsColumnNames
second_title: Aspose.Words per .NET API Reference
description: Odso proprietà. Specifica che unapplicazione di hosting deve trattare la prima riga di dati nellorigine dati esterna specificata come una riga di intestazione contenente i nomi di ciascuna colonna nellorigine dati. Il valore predefinito èfalso .
type: docs
weight: 60
url: /it/net/aspose.words.settings/odso/firstrowcontainscolumnnames/
---
## Odso.FirstRowContainsColumnNames property

Specifica che un'applicazione di hosting deve trattare la prima riga di dati nell'origine dati esterna specificata come una riga di intestazione contenente i nomi di ciascuna colonna nell'origine dati. Il valore predefinito è`falso` .

```csharp
public bool FirstRowContainsColumnNames { get; set; }
```

### Osservazioni

RK Non l'ho mai visto in uso.

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

* class [Odso](../)
* spazio dei nomi [Aspose.Words.Settings](../../odso/)
* assemblea [Aspose.Words](../../../)


