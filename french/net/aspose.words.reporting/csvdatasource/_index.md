---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words pour .NET
description: Aspose.Words.Reporting.CsvDataSource classe. Fournit un accès aux données dun fichier ou dun flux CSV à utiliser dans un rapport en C#.
type: docs
weight: 4670
url: /fr/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Fournit un accès aux données d'un fichier ou d'un flux CSV à utiliser dans un rapport.

Pour en savoir plus, visitez le[Moteur de reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article documentaire.

```csharp
public class CsvDataSource
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Crée une nouvelle source de données avec les données d'un flux CSV à l'aide des options par défaut pour l'analyse des données CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Crée une nouvelle source de données avec les données d'un fichier CSV en utilisant les options par défaut pour analyser les données CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crée une nouvelle source de données avec les données d'un flux CSV à l'aide des options spécifiées pour l'analyse des données CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crée une nouvelle source de données avec les données d'un fichier CSV à l'aide des options spécifiées pour l'analyse des données CSV. |

## Remarques

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que une source de données à l'une des[`ReportingEngine`](../reportingengine/) .BuildReport surcharges.

Dans les documents modèles, un`CsvDataSource` instance doit être traitée de la même manière que si elle était unDataTable instance . Pour plus d'informations, consultez la référence de syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

Les types de données des valeurs séparées par des virgules sont déterminés automatiquement en fonction de leurs représentations sous forme de chaîne. Ainsi, dans les documents template , vous pouvez travailler avec des valeurs saisies plutôt qu'avec de simples chaînes. Le moteur est capable de reconnaître automatiquement les valeurs des types suivants :

* Nullable
* Nullable
* Nullable
* Nullable
* String

Notez que pour que la reconnaissance automatique des types de données fonctionne, les représentations sous forme de chaîne de valeurs séparées par des virgules doivent être formées à l'aide de paramètres de culture invariants.

Pour remplacer le comportement par défaut du chargement des données CSV, initialisez et transmettez un[`CsvDataLoadOptions`](../csvdataloadoptions/) instance à un constructeur de cette classe.

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
