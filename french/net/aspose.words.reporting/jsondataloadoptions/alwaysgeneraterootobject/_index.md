---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété AlwaysGenerateRootObject de JsonDataLoadOptions améliore la gestion de vos données JSON en garantissant un objet racine cohérent pour une intégration transparente.
type: docs
weight: 20
url: /fr/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

Obtient ou définit un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine JSON . Si un élément racine JSON contient une seule propriété complexe, cet objet n'est pas créé par défaut.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
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
