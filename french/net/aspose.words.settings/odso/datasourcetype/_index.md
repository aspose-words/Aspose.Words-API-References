---
title: Odso.DataSourceType
linktitle: DataSourceType
articleTitle: DataSourceType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Odso DataSourceType pour des connexions de publipostage fluides. Spécifiez facilement des sources de données externes et optimisez votre flux de travail.
type: docs
weight: 40
url: /fr/net/aspose.words.settings/odso/datasourcetype/
---
## Odso.DataSourceType property

Spécifie le type de source de données externe à laquelle se connecter dans le cadre des informations de connexion ODSO pour ce publipostage. La valeur par défaut estDefault .

```csharp
public OdsoDataSourceType DataSourceType { get; set; }
```

## Remarques

Ce paramètre est purement une suggestion du type de source de données utilisé pour ce publipostage.

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

* enum [OdsoDataSourceType](../../odsodatasourcetype/)
* class [Odso](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
