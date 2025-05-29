---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur JsonDataLoadOptions, initialisez sans effort le chargement de vos données avec des paramètres par défaut personnalisables pour des performances optimales.
type: docs
weight: 10
url: /fr/net/aspose.words.reporting/jsondataloadoptions/jsondataloadoptions/
---
## JsonDataLoadOptions constructor

Initialise une nouvelle instance de cette classe avec les options par défaut.

```csharp
public JsonDataLoadOptions()
```

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

* class [JsonDataLoadOptions](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
