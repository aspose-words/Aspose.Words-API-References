---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words pour .NET
description: Accédez et exploitez facilement vos données CSV avec Aspose.Words.Reporting.CsvDataSource. Améliorez vos rapports grâce à une intégration transparente des données !
type: docs
weight: 5410
url: /fr/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Fournit l'accès aux données d'un fichier CSV ou d'un flux à utiliser dans un rapport.

Pour en savoir plus, visitez le[Moteur de création de rapports LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article de documentation.

```csharp
public class CsvDataSource
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Crée une nouvelle source de données avec des données provenant d'un flux CSV en utilisant les options par défaut pour l'analyse des données CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Crée une nouvelle source de données avec des données provenant d'un fichier CSV en utilisant les options par défaut pour l'analyse des données CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crée une nouvelle source de données avec des données provenant d'un flux CSV en utilisant les options spécifiées pour l'analyse des données CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crée une nouvelle source de données avec des données provenant d'un fichier CSV en utilisant les options spécifiées pour l'analyse des données CSV. |

## Remarques

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que source de données à l'un des[`ReportingEngine`](../reportingengine/) .BuildReport surcharges.

Dans les documents modèles, un`CsvDataSource` l'instance doit être traitée de la même manière que si elle était aDataTableInstance . Pour plus d'informations, consultez la référence de syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Les types de données des valeurs séparées par des virgules sont déterminés automatiquement à partir de leurs représentations sous forme de chaîne. Ainsi, dans les documents template , vous pouvez travailler avec des valeurs typées plutôt qu'avec de simples chaînes. Le moteur est capable de reconnaître automatiquement les valeurs des types suivants :

* Nullable
* Nullable
* Nullable
* Nullable
* String

Notez que pour que la reconnaissance automatique des types de données fonctionne, les représentations de chaîne de valeurs séparées par des virgules doivent être formées à l'aide de paramètres de culture invariants.

Pour remplacer le comportement par défaut du chargement des données CSV, initialisez et transmettez un[`CsvDataLoadOptions`](../csvdataloadoptions/) instance à un constructeur de cette classe.

## Exemples

Montre comment utiliser CSV comme source de données (chaîne).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
