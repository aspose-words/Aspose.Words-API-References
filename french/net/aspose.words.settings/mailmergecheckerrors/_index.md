---
title: MailMergeCheckErrors Enum
linktitle: MailMergeCheckErrors
articleTitle: MailMergeCheckErrors
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération Aspose.Words.MailMergeCheckErrors améliore votre processus de publipostage en signalant efficacement les erreurs Microsoft Word pour une création de documents transparente.
type: docs
weight: 6640
url: /fr/net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

Spécifie comment Microsoft Word signalera les erreurs détectées lors du publipostage.

```csharp
public enum MailMergeCheckErrors
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Simulate | `1` | Simulez la fusion et signalez les erreurs dans un nouveau document. |
| PauseOnError | `2` | Terminez la fusion et faites une pause pour signaler les erreurs. |
| CollectErrors | `3` | Terminez la fusion et signalez les erreurs dans un nouveau document. |
| Default | `2` | Égal àPauseOnError valeur. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
