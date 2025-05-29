---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser la propriété CommentChar dans CsvDataLoadOptions pour améliorer la gestion de vos données CSV. Optimisez le chargement de vos données dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

Obtient ou définit le caractère utilisé pour commenter les lignes de données CSV.

```csharp
public char CommentChar { get; set; }
```

## Remarques

La valeur par défaut est '#' (signe dièse).

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
