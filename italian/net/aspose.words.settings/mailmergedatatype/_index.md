---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.MailMergeDataType per un'integrazione perfetta di fonti dati esterne nei tuoi progetti di automazione dei documenti.
type: docs
weight: 6650
url: /it/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Specifica il tipo di un'origine dati di unione di stampa esterna.

```csharp
public enum MailMergeDataType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `-1` | Non è specificata alcuna origine dati per la stampa unione. |
| TextFile | `0` | Specifica che un dato documento è stato collegato a un file di testo tramite il sistema Dynamic Data Exchange (DDE). |
| Database | `1` | Specifica che un determinato documento è stato connesso a un database di Access tramite il sistema Dynamic Data Exchange (DDE). |
| Spreadsheet | `2` | Specifica che un dato documento è stato collegato a un foglio di calcolo Excel tramite il sistema Dynamic Data Exchange (DDE). |
| Query | `3` | Specifica che un dato documento è stato connesso a un'origine dati esterna tramite uno strumento di query esterno. |
| Odbc | `4` | Specifica che un dato documento è stato connesso a una fonte dati esterna tramite l'interfaccia Open Database Connectivity. |
| Native | `5` | Specifica che un determinato documento è stato connesso a un'origine dati esterna tramite l'interfaccia Office Data Source Object (ODSO). |
| Default | `-1` | Uguale aNone . |

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

* property [DataType](../mailmergesettings/datatype/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
