---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SimpleValueParseMode de JsonDataLoadOptions améliore l'analyse JSON des valeurs NULL, booléennes, numériques et chaînes. Optimisez le chargement de vos données dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

Obtient ou définit un mode d'analyse des valeurs JSON simples (nulles, booléennes, numériques, entières et chaînes) lors du chargement du JSON. Ce mode n'affecte pas l'analyse des valeurs date/heure. La valeur par défaut est .Loose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
