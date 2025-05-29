---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Reporting.CsvDataLoadOptions pour une analyse efficace des données CSV. Optimisez le traitement de vos documents grâce à des options personnalisables dès aujourd'hui !
type: docs
weight: 5400
url: /fr/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

Représente les options d'analyse des données CSV.

Pour en savoir plus, visitez le[Moteur de création de rapports LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article de documentation.

```csharp
public class CsvDataLoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Initialise une nouvelle instance de cette classe avec les options par défaut. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | Initialise une nouvelle instance de cette classe en spécifiant si les données CSV contiennent des noms de colonnes à la première ligne. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | Obtient ou définit le caractère utilisé pour commenter les lignes de données CSV. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Obtient ou définit le caractère à utiliser comme délimiteur de colonne. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | Obtient ou définit une valeur indiquant si le premier enregistrement de données CSV contient des noms de colonnes. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Obtient ou définit le caractère utilisé pour citer les valeurs de champ. |

## Remarques

Une instance de cette classe peut être passée aux constructeurs de[`CsvDataSource`](../csvdatasource/) .

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
