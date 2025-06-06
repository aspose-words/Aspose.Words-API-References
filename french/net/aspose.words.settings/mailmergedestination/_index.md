---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.MailMergeDestination, qui définit les résultats pour des publipostages fluides. Optimisez le traitement de vos documents dès aujourd'hui !
type: docs
weight: 6660
url: /fr/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Spécifie les résultats possibles qui peuvent être générés lorsqu'un publipostage est effectué sur un document.

```csharp
public enum MailMergeDestination
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| NewDocument | `0` | Spécifie que les applications d'hébergement conformes doivent générer de nouveaux documents en remplissant les champs d'un document donné avec des données provenant de la source de données externe spécifiée. |
| Printer | `1` | Spécifie que les applications d'hébergement conformes doivent imprimer les documents résultant du remplissage des champs d'un document donné avec des données externes provenant de la source de données externe spécifiée. |
| Email | `2` | Spécifie que les applications d'hébergement conformes doivent générer des e-mails à l'aide des documents résultant du remplissage des champs d'un document donné avec des données provenant de la source de données externe spécifiée. |
| Fax | `4` | Spécifie que les applications d'hébergement conformes doivent générer des fax à l'aide des documents résultant du remplissage des champs d'un document donné avec des données provenant de la source de données externe spécifiée. |
| Default | `0` | Égal àNewDocument valeur. |

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

* property [Destination](../mailmergesettings/destination/)
* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
