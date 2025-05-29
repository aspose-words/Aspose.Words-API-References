---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words pour .NET
description: Créez facilement une source de données CSV puissante grâce à notre constructeur CsvDataSource. Simplifiez l'analyse des données grâce aux options par défaut pour une intégration fluide.
type: docs
weight: 10
url: /fr/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Crée une nouvelle source de données avec des données provenant d'un fichier CSV en utilisant les options par défaut pour l'analyse des données CSV.

```csharp
public CsvDataSource(string csvPath)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| csvPath | String | Le chemin d’accès au fichier CSV à utiliser comme source de données. |

### Voir également

* class [CsvDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Crée une nouvelle source de données avec des données provenant d'un fichier CSV en utilisant les options spécifiées pour l'analyse des données CSV.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| csvPath | String | Le chemin d’accès au fichier CSV à utiliser comme source de données. |
| options | CsvDataLoadOptions | Options d'analyse des données CSV. |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Crée une nouvelle source de données avec des données provenant d'un flux CSV en utilisant les options par défaut pour l'analyse des données CSV.

```csharp
public CsvDataSource(Stream csvStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| csvStream | Stream | Le flux de données CSV à utiliser comme source de données. |

### Voir également

* class [CsvDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Crée une nouvelle source de données avec des données provenant d'un flux CSV en utilisant les options spécifiées pour l'analyse des données CSV.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| csvStream | Stream | Le flux de données CSV à utiliser comme source de données. |
| options | CsvDataLoadOptions | Options d'analyse des données CSV. |

## Exemples

Montre comment utiliser CSV comme source de données (flux).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### Voir également

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
