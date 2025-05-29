---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HasHeaders de CsvDataLoadOptions pour gérer facilement les importations CSV en spécifiant si le premier enregistrement inclut des noms de colonnes pour une intégration transparente des données.
type: docs
weight: 40
url: /fr/net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

Obtient ou définit une valeur indiquant si le premier enregistrement de données CSV contient des noms de colonnes.

```csharp
public bool HasHeaders { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

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
