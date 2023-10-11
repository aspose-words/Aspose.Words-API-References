---
title: Class JsonDataLoadOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Reporting.JsonDataLoadOptions classe. Représente les options danalyse des données JSON.
type: docs
weight: 4680
url: /fr/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Représente les options d'analyse des données JSON.

Pour en savoir plus, visitez le[Moteur de reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article documentaire.

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
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Obtient ou définit un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément JSON root . Si un élément racine JSON contient une seule propriété complexe, un tel objet n'est pas créé par défaut. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Obtient ou définit les formats exacts pour analyser les valeurs date-heure JSON lors du chargement de JSON. La valeur par défaut est`nul` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Obtient ou définit un indicateur indiquant si les espaces de début et de fin doivent être conservés lors du chargement des valeurs string des données JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Obtient ou définit un mode d'analyse des valeurs simples JSON (null, booléen, nombre, entier et chaîne) lors du chargement de JSON. Un tel mode n'affecte pas l'analyse des valeurs date-heure. La valeur par défaut est Loose . |

### Remarques

Une instance de cette classe peut être transmise aux constructeurs de[`JsonDataSource`](../jsondatasource/) .

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)


