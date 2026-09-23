---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words pour Java"
description: "Fournit l'accès aux données d'un fichier ou d'un flux JSON à utiliser dans un rapport en Java."
type: docs
weight: 409
url: /fr/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Fournit l'accès aux données d'un fichier ou d'un flux JSON à utiliser dans un rapport.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que source de données à l'une des surcharges de [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport.

Dans les documents modèles, si un élément JSON de niveau supérieur est un tableau, une instance de [JsonDataSource](../../com.aspose.words/jsondatasource/) doit être traitée de la même manière qu'une instance de [DataTable](../../com.aspose.words.net.system.data/datatable/). Si un élément JSON de niveau supérieur est un objet, une instance de [JsonDataSource](../../com.aspose.words/jsondatasource/) doit être traitée de la même manière qu'une instance de [DataRow](../../com.aspose.words.net.system.data/datarow/). Pour plus d'informations, consultez la référence de la syntaxe du modèle (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Dans les documents modèles, vous pouvez travailler avec les valeurs typées des éléments JSON. Pour plus de commodité, le moteur remplace l'ensemble des types simples JSON par le suivant :

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Le moteur reconnaît automatiquement les valeurs des types supplémentaires à partir de leurs représentations JSON.

Pour remplacer le comportement par défaut du chargement des données JSON, initialisez et transmettez une instance de [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) au constructeur de cette classe.

 **Examples:** 

Montre comment utiliser JSON comme source de données (chaîne).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options par défaut pour l'analyse des données JSON. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Initialise une nouvelle instance de cette classe. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options spécifiées pour l'analyse des données JSON. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Initialise une nouvelle instance de cette classe. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options par défaut pour l'analyse des données JSON.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| jsonPath | java.lang.String | Le chemin du fichier JSON à utiliser comme source de données. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options spécifiées pour l'analyse des données JSON.

 **Examples:** 

Montre comment utiliser JSON comme source de données (chaîne).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| jsonPath | java.lang.String | Le chemin du fichier JSON à utiliser comme source de données. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | Options pour l'analyse des données JSON. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

