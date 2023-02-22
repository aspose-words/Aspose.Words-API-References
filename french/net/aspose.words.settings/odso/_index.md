---
title: Class Odso
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Settings.Odso classe. Spécifie les paramètres Office Data Source Object ODSO pour une source de données de fusion et publipostage.
type: docs
weight: 5580
url: /fr/net/aspose.words.settings/odso/
---
## Odso class

Spécifie les paramètres Office Data Source Object (ODSO) pour une source de données de fusion et publipostage.

```csharp
public class Odso
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Odso](odso/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Spécifie le caractère qui doit être interprété comme le délimiteur de colonne utilisé pour séparer les colonnes dans les sources de données externes. La valeur par défaut est 0, ce qui signifie qu'aucun délimiteur de colonne n'est défini. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer le publipostage. La valeur par défaut est une chaîne vide. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Spécifie le type de source de données externe à laquelle se connecter dans le cadre des informations de connexion ODSO pour ce publipostage. La valeur par défaut estDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Obtient ou définit une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. Cet objet n'est jamais null. |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Spécifie qu'une application d'hébergement doit traiter la première ligne de données dans la source de données externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne dans la source de données. La valeur par défaut est`faux` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Obtient ou définit une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans le publipostage. Cet objet n'est jamais null. |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Spécifie l'ensemble de données particulier auquel une source doit être connectée au sein d'une source de données externe. La valeur par défaut est une chaîne vide. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Spécifie la chaîne de connexion UDL (Universal Data Link) utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Renvoie un clone profond de cet objet. |

### Remarques

ODSO semble être la "nouvelle" façon que les nouvelles versions de Microsoft Word préfèrent utiliser lors de la spécification de certains types de sources de données pour un document de fusion et publipostage. ODSO est probablement apparu pour la première fois dans Microsoft Word 2000.

L'utilisation d'ODSO est mal documentée et la meilleure façon d'apprendre à utiliser les propriétés de cet objet est de créer manuellement un document avec une source de données souhaitée dans Microsoft Word, puis d'ouvrir ce document à l'aide de Aspose.Words et d'examiner les propriétés de la[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) et [`Odso`](../mailmergesettings/odso/) objets. C'est une bonne approche à adopter si vous voulez apprendre à configurer par programme une source de données, par exemple.

Vous n'avez normalement pas besoin de créer directement des objets de cette classe car les paramètres ODSO sont toujours disponibles via le[`Odso`](../mailmergesettings/odso/) propriété.

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

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)


