---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Reporting.JsonSimpleValueParseMode pour une analyse JSON efficace. Gérez facilement les valeurs nulles, les booléens, les nombres et les chaînes !
type: docs
weight: 5440
url: /fr/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Spécifie un mode d'analyse des valeurs JSON simples (null, booléen, nombre, entier et chaîne) lors du chargement de JSON. Ce mode n'affecte pas l'analyse des valeurs date-heure.

```csharp
public enum JsonSimpleValueParseMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Loose | `0` | Spécifie le mode dans lequel les types de valeurs simples JSON sont déterminés lors de l'analyse de leurs représentations de chaîne. Par exemple, le type de 'prop' de l'extrait JSON '{prop: "123" }' est déterminé comme un entier dans ce mode. |
| Strict | `1` | Spécifie le mode dans lequel les types de valeurs simples JSON sont déterminés à partir de la notation JSON elle-même. Par exemple, le type de « prop » de l'extrait JSON « { prop: "123" } » est déterminé comme une chaîne dans ce mode. |

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

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
