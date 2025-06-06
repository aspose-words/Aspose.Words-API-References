---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.MailMergeMainDocumentType, che definisce vari tipi di documenti sorgente per la stampa unione, per un'automazione ottimale dei documenti.
type: docs
weight: 6670
url: /it/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Specifica i tipi possibili per un documento sorgente di stampa unione.

```csharp
public enum MailMergeMainDocumentType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| NotAMergeDocument | `0` | Questo documento non è un documento di stampa unione. |
| FormLetters | `1` | Specifica che il documento di origine della stampa unione è di tipo lettera standard. |
| MailingLabels | `2` | Specifica che il documento di origine della stampa unione è di tipo etichetta postale. |
| Envelopes | `4` | Specifica che il documento di origine della stampa unione è di tipo busta. |
| Catalog | `8` | Specifica che il documento di origine della stampa unione è di tipo catalogo. |
| Email | `16` | Specifica che il documento di origine della stampa unione è di tipo messaggio di posta elettronica. |
| Fax | `32` | Specifica che il documento di origine della stampa unione è di tipo fax. |
| Default | `0` | Uguale aNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
