---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words OdsoDataSourceType per connetterti facilmente a fonti dati esterne, migliorando le tue capacità di elaborazione dei documenti.
type: docs
weight: 6720
url: /it/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Specifica il tipo di origine dati esterna a cui connettersi come parte delle informazioni di connessione ODSO.

```csharp
public enum OdsoDataSourceType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Text | `0` | Specifica che un dato documento è stato collegato a un file di testo. Eventualmente wdMergeSubTypeOther. |
| Database | `1` | Specifica che un dato documento è stato connesso a un database. Eventualmente wdMergeSubTypeAccess. |
| AddressBook | `2` | Specifica che un dato documento è stato collegato a una rubrica di contatti. Eventualmente wdMergeSubTypeOAL. |
| Document1 | `3` | Specifica che un dato documento è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. Eventualmente wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Specifica che un dato documento è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. Eventualmente wdMergeSubTypeWorks. |
| Native | `5` | Specifica che un dato documento è stato collegato a un altro formato di documento nativo dell'applicazione produttrice. Eventualmente wdMergeSubTypeOLEDBText |
| Email | `6` | Specifica che un determinato documento è stato collegato a un'applicazione di posta elettronica. Eventualmente wdMergeSubTypeOutlook. |
| None | `7` | Il tipo di origine dati esterna non è specificato. Forse wdMergeSubTypeWord. |
| Legacy | `8` | Specifica che un dato documento è stato collegato a un formato di documento legacy supportato dall'applicazione produttrice Eventualmente wdMergeSubTypeWord2000. |
| Master | `9` | Specifica che un dato documento è stato collegato a un'origine dati che aggrega altre origini dati. |
| Default | `7` | Uguale aNone . |

## Osservazioni

La specifica OOXML è molto vaga per questo enum. Immagino che possa corrispondere all'enumerazione WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.

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
