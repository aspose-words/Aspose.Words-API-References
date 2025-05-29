---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words pour .NET
description: Bénéficiez de rapports performants avec Aspose.Words.Reporting.JsonDataSource. Accédez facilement aux données JSON pour une intégration transparente à vos rapports.
type: docs
weight: 5430
url: /fr/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Fournit l'accès aux données d'un fichier ou d'un flux JSON à utiliser dans un rapport.

Pour en savoir plus, visitez le[Moteur de création de rapports LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article de documentation.

```csharp
public class JsonDataSource
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Crée une nouvelle source de données avec des données provenant d'un flux JSON en utilisant les options par défaut pour l'analyse des données JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options par défaut pour l'analyse des données JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crée une nouvelle source de données avec des données provenant d'un flux JSON en utilisant les options spécifiées pour l'analyse des données JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crée une nouvelle source de données avec des données provenant d'un fichier JSON en utilisant les options spécifiées pour l'analyse des données JSON. |

## Remarques

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que source de données à l'un des[`ReportingEngine`](../reportingengine/) .BuildReport surcharges.

Dans les documents modèles, si un élément JSON de niveau supérieur est un tableau, un`JsonDataSource` l'instance doit être traitée de la même manière que s'il s'agissait d'unDataTableInstance . Si un élément JSON de niveau supérieur est un objet, un`JsonDataSource` l'instance doit être traitée de la même manière que si elle était uneDataRow Instance . Pour plus d'informations, consultez la référence de syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Dans les documents modèles, vous pouvez utiliser des valeurs typées d'éléments JSON. Pour plus de commodité, le moteur remplace l'ensemble de types JSON simples par le suivant :

* Nullable
* Nullable
* Nullable
* Nullable
* String

Le moteur reconnaît automatiquement les valeurs des types supplémentaires sur leurs représentations JSON.

Pour remplacer le comportement par défaut du chargement des données JSON, initialisez et transmettez un[`JsonDataLoadOptions`](../jsondataloadoptions/) instance à un constructeur de cette classe.

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
