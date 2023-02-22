---
title: MailMergeSettings.Query
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMergeSettings propriété. Contient la chaîne de langage de requête structuré qui doit être exécutée sur la source de données externe spécifiée pour renvoyer lensemble denregistrements qui doivent être importés dans le document lors de lopération de fusion et publipostage. La valeur par défaut est une chaîne vide.
type: docs
weight: 160
url: /fr/net/aspose.words.settings/mailmergesettings/query/
---
## MailMergeSettings.Query property

Contient la chaîne de langage de requête structuré qui doit être exécutée sur la source de données externe spécifiée pour renvoyer l'ensemble d'enregistrements qui doivent être importés dans le document lors de l'opération de fusion et publipostage. La valeur par défaut est une chaîne vide.

```csharp
public string Query { get; set; }
```

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

* class [MailMergeSettings](../)
* espace de noms [Aspose.Words.Settings](../../mailmergesettings/)
* Assemblée [Aspose.Words](../../../)


