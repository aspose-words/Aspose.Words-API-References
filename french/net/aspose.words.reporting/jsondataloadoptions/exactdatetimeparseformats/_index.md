---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words pour .NET
description: Découvrez ExactDateTimeParseFormats de JsonDataLoadOptions pour une analyse précise des dates et heures JSON. Personnalisez facilement les formats pour un chargement fluide des données !
type: docs
weight: 30
url: /fr/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Obtient ou définit les formats exacts pour l'analyse des valeurs date-heure JSON lors du chargement du fichier JSON. La valeur par défaut est`nul` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Remarques

Les chaînes encodées au format date/heure Microsoft® JSON (par exemple, « /Date(1224043200000)/ ») sont toujours reconnues comme des valeurs date/heure, quelle que soit la valeur de cette propriété. Cette propriété définit des formats supplémentaires à utiliser lors de l'analyse des valeurs date/heure des chaînes, comme suit :

* Quand`ExactDateTimeParseFormats` est`nul` , le format ISO-8601 et tous les formats de date-heure pris en charge pour les cultures actuelles, anglaise américaine et anglaise néo-zélandaise sont utilisés en plus dans l'ordre mentionné.
* Quand`ExactDateTimeParseFormats`contient des chaînes, elles sont utilisées comme formats date-heure supplémentaires utilisant la culture actuelle.
* Quand`ExactDateTimeParseFormats` est vide, aucun format de date-heure supplémentaire n'est utilisé.

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
