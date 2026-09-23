---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words pour Java"
description: "Fournit un accès aux données d'un fichier CSV ou d'un flux à utiliser dans un rapport en Java."
type: docs
weight: 138
url: /fr/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Fournit l'accès aux données d'un fichier CSV ou d'un flux à utiliser dans un rapport.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que source de données à l'une des surcharges de [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport.

Dans les documents modèles, une instance de [CsvDataSource](../../com.aspose.words/csvdatasource/) doit être traitée de la même manière que s'il s'agissait d'une instance de [DataTable](../../com.aspose.words.net.system.data/datatable/). Pour plus d'informations, consultez la référence de la syntaxe des modèles (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Les types de données des valeurs séparées par des virgules sont déterminés automatiquement à partir de leurs représentations sous forme de chaîne. Ainsi, dans les documents modèles, vous pouvez travailler avec des valeurs typées plutôt qu'avec de simples chaînes. Le moteur est capable de reconnaître automatiquement les valeurs des types suivants :

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Notez que, pour que la reconnaissance automatique des types de données fonctionne, les représentations sous forme de chaîne des valeurs séparées par des virgules doivent être générées en utilisant les paramètres culturels invariants.

Pour remplacer le comportement par défaut du chargement des données CSV, initialisez et transmettez une instance de [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) à un constructeur de cette classe.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | Crée une nouvelle source de données avec les données d'un fichier CSV en utilisant les options par défaut pour l'analyse des données CSV. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier CSV en utilisant les options spécifiées pour l'analyse des données CSV. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Initialise une nouvelle instance de cette classe. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Initialise une nouvelle instance de cette classe. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


Crée une nouvelle source de données avec les données d'un fichier CSV en utilisant les options par défaut pour l'analyse des données CSV.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| csvPath | java.lang.String | Le chemin du fichier CSV à utiliser comme source de données. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Crée une nouvelle source de données avec les données d'un fichier CSV en utilisant les options spécifiées pour l'analyse des données CSV.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| csvPath | java.lang.String | Le chemin du fichier CSV à utiliser comme source de données. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | Options pour analyser les données CSV. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

