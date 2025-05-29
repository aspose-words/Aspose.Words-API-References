---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.MailMergeSettings pour rationaliser l'automatisation des documents avec de puissantes fonctionnalités de publipostage pour une efficacité accrue.
type: docs
weight: 6680
url: /fr/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Spécifie toutes les informations de publipostage pour un document.

Pour en savoir plus, visitez le[Fusion et publipostage et création de rapports](https://docs.aspose.com/words/net/mail-merge-and-reporting/) article de documentation.

```csharp
public class MailMergeSettings
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Spécifie l'index de base 1 de l'enregistrement de la source de données, qui sera affiché dans Microsoft Word. La valeur par défaut est 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Spécifie la colonne de la source de données contenant les adresses e-mail. La valeur par défaut est une chaîne vide. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Spécifie le type de rapport d'erreur qui doit être effectué par Microsoft Word lors de l'exécution d'un publipostage. La valeur par défaut estDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Spécifie le chemin d'accès à la source de données de publipostage. La valeur par défaut est une chaîne vide. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Spécifie le type de source de données de publipostage et la méthode d'accès aux données. La valeur par défaut estDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Spécifie comment Microsoft Word affichera les résultats d'un publipostage. La valeur par défaut estDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Spécifie comment une application effectuant le publipostage doit gérer les lignes vides dans les documents fusionnés résultant du publipostage. La valeur par défaut est`FAUX` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Spécifie le chemin d'accès à la source de l'en-tête de publipostage. La valeur par défaut est une chaîne vide. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Je ne suis pas sûr de cela. La référence d'automatisation Microsoft Word suggère que cela spécifie que la requête est exécutée à chaque ouverture du document dans Microsoft Word. Mais la spécification OOXML suggère que cela spécifie que la requête contient une référence à un fichier de requête externe contenant la requête réelle. La valeur par défaut est`FAUX` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Spécifie que les documents produits lors d'une opération de publipostage doivent être envoyés par courriel en pièce jointe plutôt que dans le corps du courriel. La valeur par défaut est`FAUX` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Spécifie le texte qui doit apparaître dans la ligne d'objet des e-mails ou des fax produits lors du publipostage. La valeur par défaut est une chaîne vide. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Spécifie le type de document principal de fusion et publipostage. La valeur par défaut estDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Obtient ou définit l'objet qui spécifie les paramètres de l'objet source de données Office (ODSO). |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Contient la chaîne de langage de requête structuré qui doit être exécutée sur la source de données externe spécifiée pour renvoyer l'ensemble des enregistrements qui doivent être importés dans le document lorsque l'opération de publipostage est effectuée. La valeur par défaut est une chaîne vide. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée où les champs de fusion ont été insérés (par exemple, aperçu des données fusionnées). La valeur par défaut est`FAUX` . |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Efface les paramètres de publipostage de telle manière que lorsque le document est enregistré, aucun paramètre de publipostage ne sera enregistré et il deviendra un document normal. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Renvoie un clone profond de cet objet. |

## Remarques

Vous pouvez utiliser cet objet pour spécifier une source de données de publipostage pour un document et ces informations (ainsi que les champs de données disponibles) apparaîtront dans Microsoft Word lorsque l'utilisateur ouvrira ce document. Ou vous pouvez utiliser cet objet pour interroger les paramètres de publipostage que l'utilisateur a spécifiés dans Microsoft Word pour ce document.

Vous n'avez normalement pas besoin de créer directement des objets de cette classe car les paramètres de publipostage d'un document sont toujours disponibles via le[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) propriété.

Pour détecter si ce document est un document principal de publipostage, vérifiez la valeur de [`MainDocumentType`](./maindocumenttype/) propriété.

Pour supprimer les paramètres de publipostage et les informations sur la source de données d'un document, vous pouvez utiliser [`Clear`](./clear/) méthode. Aspose.Words n'écrira pas les paramètres de publipostage dans un document si le[`MainDocumentType`](./maindocumenttype/) la propriété est définie surNotAMergeDocument ou le[`DataType`](./datatype/) la propriété est définie surNone.

La meilleure façon d'apprendre à utiliser les propriétés de cet objet est de créer manuellement un document avec une source de données souhaitée dans Microsoft Word, puis d'ouvrir ce document à l'aide d'Aspose.Words et d'examiner les propriétés de l'objet.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) et[`Odso`](./odso/) objets. C'est une bonne approche à adopter si vous souhaitez apprendre à configurer une source de données par programmation, par exemple.

Aspose.Words conserve les informations de publipostage lors du chargement, de l'enregistrement et de la conversion de documents entre différents formats, mais n'utilise pas ces informations lors de l'exécution de son propre publipostage à l'aide de[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) objet.

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
