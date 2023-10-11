---
title: Class JsonDataSource
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Reporting.JsonDataSource classe. Fournit un accès aux données dun fichier ou dun flux JSON à utiliser dans un rapport.
type: docs
weight: 4690
url: /fr/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Fournit un accès aux données d'un fichier ou d'un flux JSON à utiliser dans un rapport.

Pour en savoir plus, visitez le[Moteur de reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article documentaire.

```csharp
public class JsonDataSource
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | Crée une nouvelle source de données avec les données d'un flux JSON à l'aide des options par défaut pour analyser les données JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options par défaut pour analyser les données JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | Crée une nouvelle source de données avec les données d'un flux JSON à l'aide des options spécifiées pour l'analyse des données JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier JSON à l'aide des options spécifiées pour l'analyse des données JSON. |

### Remarques

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que une source de données à l'une des[`ReportingEngine`](../reportingengine/) .BuildReport surcharges.

Dans les documents modèles, si un élément JSON de niveau supérieur est un tableau, un`JsonDataSource` instance doit être traitée de la même manière que s'il s'agissait d'unDataTable instance . Si un élément JSON de niveau supérieur est un objet, un`JsonDataSource` instance doit être traitée de la même manière que s'il s'agissait de unDataRow instance . Pour plus d'informations, consultez la référence de syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

Dans les documents modèles, vous pouvez travailler avec des valeurs saisies d'éléments JSON. Pour plus de commodité, le moteur remplace l'ensemble de types simples JSON par le suivant :

* Nullable
* Nullable
* Nullable
* Nullable
* String

Le moteur reconnaît automatiquement les valeurs des types supplémentaires sur leurs représentations JSON.

Pour remplacer le comportement par défaut du chargement des données JSON, initialisez et transmettez un[`JsonDataLoadOptions`](../jsondataloadoptions/) instance à un constructeur de cette classe.

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)


