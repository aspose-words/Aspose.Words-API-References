---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Délimiteur CsvDataLoadOptions pour personnaliser facilement les délimiteurs de colonnes et optimiser le chargement des données. Optimisez votre gestion de données dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Obtient ou définit le caractère à utiliser comme délimiteur de colonne.

```csharp
public char Delimiter { get; set; }
```

## Remarques

La valeur par défaut est ',' (virgule).

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

* class [CsvDataLoadOptions](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
