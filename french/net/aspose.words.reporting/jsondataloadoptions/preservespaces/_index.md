---
title: JsonDataLoadOptions.PreserveSpaces
linktitle: PreserveSpaces
articleTitle: PreserveSpaces
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété JsonDataLoadOptions PreserveSpaces améliore la gestion des données JSON en préservant les espaces de début et de fin pour des valeurs de chaîne précises.
type: docs
weight: 40
url: /fr/net/aspose.words.reporting/jsondataloadoptions/preservespaces/
---
## JsonDataLoadOptions.PreserveSpaces property

Obtient ou définit un indicateur indiquant si les espaces de début et de fin doivent être conservés lors du chargement des valeurs string des données JSON.

```csharp
public bool PreserveSpaces { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

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
