---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Reporting.JsonDataLoadOptions pour une analyse fluide des données JSON. Optimisez le traitement de vos documents grâce à des options flexibles !
type: docs
weight: 5420
url: /fr/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Représente les options d'analyse des données JSON.

Pour en savoir plus, visitez le[Moteur de création de rapports LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article de documentation.

```csharp
public class JsonDataLoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Initialise une nouvelle instance de cette classe avec les options par défaut. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Obtient ou définit un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine JSON . Si un élément racine JSON contient une seule propriété complexe, cet objet n'est pas créé par défaut. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Obtient ou définit les formats exacts pour l'analyse des valeurs date-heure JSON lors du chargement du fichier JSON. La valeur par défaut est`nul` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Obtient ou définit un indicateur indiquant si les espaces de début et de fin doivent être conservés lors du chargement des valeurs string des données JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Obtient ou définit un mode d'analyse des valeurs JSON simples (nulles, booléennes, numériques, entières et chaînes) lors du chargement du JSON. Ce mode n'affecte pas l'analyse des valeurs date/heure. La valeur par défaut est .Loose . |

## Remarques

Une instance de cette classe peut être passée aux constructeurs de[`JsonDataSource`](../jsondatasource/) .

## Exemples

Montre comment utiliser JSON comme source de données (chaîne).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
