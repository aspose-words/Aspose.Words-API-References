---
title: Enum MailMergeMainDocumentType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Settings.MailMergeMainDocumentType énumération. Spécifie les types possibles pour un document source de fusion et publipostage.
type: docs
weight: 5540
url: /fr/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Spécifie les types possibles pour un document source de fusion et publipostage.

```csharp
public enum MailMergeMainDocumentType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| NotAMergeDocument | `0` | Ce document n'est pas un document de publipostage. |
| FormLetters | `1` | Spécifie que le document source de fusion et publipostage est du type lettre type. |
| MailingLabels | `2` | Spécifie que le document source de fusion et publipostage est du type d'étiquette de publipostage. |
| Envelopes | `4` | Spécifie que le document source de fusion et publipostage est du type enveloppe. |
| Catalog | `8` | Spécifie que le document source de fusion et publipostage est de type catalogue. |
| Email | `16` | Spécifie que le document source de fusion et publipostage est du type de message électronique. |
| Fax | `32` | Spécifie que le document source de fusion et publipostage est du type fax. |
| Default | `0` | Égal àNotAMergeDocument |

### Exemples

Montre comment exécuter un publipostage avec des données provenant d'un objet de source de données Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Crée une source de données sous la forme d'un fichier ASCII, avec le "|" personnage
// agissant comme le délimiteur qui sépare les colonnes. La première ligne contient les noms des trois colonnes,
// et chaque ligne suivante est une ligne avec leurs valeurs respectives.
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

// L'ouverture de ce document dans Microsoft Word exécutera le publipostage avant d'afficher le contenu. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Voir également

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)


