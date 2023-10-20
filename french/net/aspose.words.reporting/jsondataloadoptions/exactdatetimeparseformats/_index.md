---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words pour .NET
description: JsonDataLoadOptions ExactDateTimeParseFormats propriété. Obtient ou définit les formats exacts pour analyser les valeurs dateheure JSON lors du chargement de JSON. La valeur par défaut estnul  en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Obtient ou définit les formats exacts pour analyser les valeurs date-heure JSON lors du chargement de JSON. La valeur par défaut est`nul` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Remarques

Les chaînes codées à l'aide du format date-heure Microsoft® JSON (par exemple, "/Date(1224043200000)/") sont toujours reconnues comme valeurs date-heure, quelle que soit la valeur de cette propriété. La propriété définit des formats supplémentaires à utiliser lors de l'analyse des valeurs date-heure des chaînes de la manière suivante :

* Quand`ExactDateTimeParseFormats` est`nul` le format ISO-8601 et tous les formats date-heure pris en charge pour les cultures actuelles, anglais des États-Unis et anglais de la Nouvelle-Zélande, sont utilisés en plus dans dans l'ordre mentionné.
* Quand`ExactDateTimeParseFormats` contient des chaînes, elles sont utilisées comme formats date-time supplémentaires utilisant la culture actuelle.
* Quand`ExactDateTimeParseFormats` est vide, aucun format date-heure supplémentaire n'est utilisé.

### Voir également

* class [JsonDataLoadOptions](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
