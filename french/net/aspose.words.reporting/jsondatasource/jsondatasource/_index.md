---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words pour .NET
description: Créez sans effort une source de données puissante avec le constructeur JsonDataSource, permettant une intégration transparente des fichiers JSON et une analyse optimisée des données.
type: docs
weight: 10
url: /fr/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Crée une nouvelle source de données avec les données d'un fichier JSON en utilisant les options par défaut pour l'analyse des données JSON.

```csharp
public JsonDataSource(string jsonPath)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| jsonPath | String | Le chemin vers le fichier JSON à utiliser comme source de données. |

### Voir également

* class [JsonDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Crée une nouvelle source de données avec des données provenant d'un flux JSON en utilisant les options par défaut pour l'analyse des données JSON.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| jsonStream | Stream | Le flux de données JSON à utiliser comme source de données. |

### Voir également

* class [JsonDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Crée une nouvelle source de données avec des données provenant d'un fichier JSON en utilisant les options spécifiées pour l'analyse des données JSON.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| jsonPath | String | Le chemin vers le fichier JSON à utiliser comme source de données. |
| options | JsonDataLoadOptions | Options d'analyse des données JSON. |

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

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Crée une nouvelle source de données avec des données provenant d'un flux JSON en utilisant les options spécifiées pour l'analyse des données JSON.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| jsonStream | Stream | Le flux de données JSON à utiliser comme source de données. |
| options | JsonDataLoadOptions | Options d'analyse des données JSON. |

## Exemples

Montre comment utiliser JSON comme source de données (flux).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"}
};

using (FileStream stream = File.OpenRead(MyDir + "List of people.json"))
{
    JsonDataSource dataSource = new JsonDataSource(stream, options);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataStream.docx");
```

### Voir également

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
