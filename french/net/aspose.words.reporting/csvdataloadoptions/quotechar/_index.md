---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words pour .NET
description: Découvrez la propriété QuoteChar de CsvDataLoadOptions pour personnaliser facilement la citation des valeurs de champ pour une gestion transparente des données et une gestion CSV améliorée.
type: docs
weight: 50
url: /fr/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

Obtient ou définit le caractère utilisé pour citer les valeurs de champ.

```csharp
public char QuoteChar { get; set; }
```

## Remarques

La valeur par défaut est '"' (guillemets).

Doublez le caractère pour le placer dans un texte cité.

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
