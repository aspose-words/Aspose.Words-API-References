---
title: Odso.FirstRowContainsColumnNames
linktitle: FirstRowContainsColumnNames
articleTitle: FirstRowContainsColumnNames
second_title: Aspose.Words pour .NET
description: Odso FirstRowContainsColumnNames propriété. Spécifie quune application dhébergement doit traiter la première ligne de données de la source data externe spécifiée comme une ligne dentête contenant les noms de chaque colonne de la source de données. La valeur par défaut estFAUX  en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.settings/odso/firstrowcontainscolumnnames/
---
## Odso.FirstRowContainsColumnNames property

Spécifie qu'une application d'hébergement doit traiter la première ligne de données de la source data externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne de la source de données. La valeur par défaut est`FAUX` .

```csharp
public bool FirstRowContainsColumnNames { get; set; }
```

## Remarques

RK Je n'ai jamais vu cela utilisé.

## Exemples

Montre comment exécuter un publipostage avec des données provenant d’un objet source de données Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Crée une source de données sous forme de fichier ASCII, avec le "|" personnage
// agissant comme délimiteur qui sépare les colonnes. La première ligne contient les noms des trois colonnes,
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

* class [Odso](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
