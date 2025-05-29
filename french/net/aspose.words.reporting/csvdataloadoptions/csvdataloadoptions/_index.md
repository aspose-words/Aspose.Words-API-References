---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur CsvDataLoadOptions : initialisez facilement avec les paramètres par défaut pour un chargement de données efficace et une intégration transparente.
type: docs
weight: 10
url: /fr/net/aspose.words.reporting/csvdataloadoptions/csvdataloadoptions/
---
## CsvDataLoadOptions() {#constructor}

Initialise une nouvelle instance de cette classe avec les options par défaut.

```csharp
public CsvDataLoadOptions()
```

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

---

## CsvDataLoadOptions(*bool*) {#constructor_1}

Initialise une nouvelle instance de cette classe en spécifiant si les données CSV contiennent des noms de colonnes à la première ligne.

```csharp
public CsvDataLoadOptions(bool hasHeaders)
```

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
