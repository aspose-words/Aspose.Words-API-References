---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.MailMergeDataType pour une intégration transparente de sources de données externes dans vos projets d'automatisation de documents.
type: docs
weight: 6650
url: /fr/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Spécifie le type d'une source de données de publipostage externe.

```csharp
public enum MailMergeDataType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `-1` | Aucune source de données de publipostage n'est spécifiée. |
| TextFile | `0` | Spécifie qu'un document donné a été connecté à un fichier texte via le système d'échange dynamique de données (DDE). |
| Database | `1` | Spécifie qu'un document donné a été connecté à une base de données Access via le système Dynamic Data Exchange (DDE). |
| Spreadsheet | `2` | Spécifie qu'un document donné a été connecté à une feuille de calcul Excel via le système Dynamic Data Exchange (DDE). |
| Query | `3` | Spécifie qu'un document donné a été connecté à une source de données externe à l'aide d'un outil de requête externe. |
| Odbc | `4` | Spécifie qu'un document donné a été connecté à une source de données externe via l'interface Open Database Connectivity. |
| Native | `5` | Spécifie qu'un document donné a été connecté à une source de données externe via l'interface Office Data Source Object (ODSO). |
| Default | `-1` | Égal àNone . |

## Exemples

Montre comment exécuter un publipostage avec des données provenant d'un objet source de données Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Créer une source de données sous la forme d'un fichier ASCII, avec le caractère "|"
// agit comme séparateur de colonnes. La première ligne contient les noms des trois colonnes.
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

* property [DataType](../mailmergesettings/datatype/)
* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
