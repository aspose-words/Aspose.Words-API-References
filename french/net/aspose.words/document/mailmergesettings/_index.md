---
title: Document.MailMergeSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient ou définit lobjet qui contient toutes les informations de publipostage pour un document.
type: docs
weight: 270
url: /fr/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Obtient ou définit l'objet qui contient toutes les informations de publipostage pour un document.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

### Remarques

Vous pouvez utiliser cet objet pour spécifier une source de données de publipostage pour un document et ces informations (ainsi que les champs de données disponibles) apparaîtront dans Microsoft Word lorsque l'utilisateur ouvrira ce document. Ou vous pouvez utiliser cet objet pour interroger les paramètres de fusion et de publipostage. que l'utilisateur a spécifié dans Microsoft Word pour ce document.

Cet objet n'est jamais`nul`.

### Exemples

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


