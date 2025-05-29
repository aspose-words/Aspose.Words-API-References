---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words OdsoDataSourceType pour vous connecter facilement à des sources de données externes, améliorant ainsi vos capacités de traitement de documents.
type: docs
weight: 6720
url: /fr/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Spécifie le type de source de données externe à laquelle se connecter dans le cadre des informations de connexion ODSO.

```csharp
public enum OdsoDataSourceType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Text | `0` | Spécifie qu'un document donné a été connecté à un fichier texte. Éventuellement wdMergeSubTypeOther. |
| Database | `1` | Spécifie qu'un document donné a été connecté à une base de données. Éventuellement wdMergeSubTypeAccess. |
| AddressBook | `2` | Spécifie qu'un document donné a été connecté à un carnet d'adresses de contacts. Éventuellement wdMergeSubTypeOAL. |
| Document1 | `3` | Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. Éventuellement wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. Éventuellement wdMergeSubTypeWorks. |
| Native | `5` | Spécifie qu'un document donné a été connecté à un autre format de document natif de l'application productrice. Éventuellement wdMergeSubTypeOLEDBText |
| Email | `6` | Spécifie qu'un document donné a été connecté à une application de messagerie. Éventuellement wdMergeSubTypeOutlook. |
| None | `7` | Le type de la source de données externe n'est pas spécifié. Éventuellement wdMergeSubTypeWord. |
| Legacy | `8` | Spécifie qu'un document donné a été connecté à un format de document hérité pris en charge par l'application productrice Éventuellement wdMergeSubTypeWord2000. |
| Master | `9` | Spécifie qu'un document donné a été connecté à une source de données qui regroupe d'autres sources de données. |
| Default | `7` | Égal àNone . |

## Remarques

La spécification OOXML est très vague pour cette énumération. Je suppose qu'elle correspond à l'énumération WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.

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

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
