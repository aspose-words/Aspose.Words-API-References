---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words LowCode ReportBuilderOptions, conçue pour améliorer votre expérience LINQ Reporting Engine avec des options personnalisables pour une génération de documents transparente.
type: docs
weight: 4380
url: /fr/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Représente les options pour la fonctionnalité LINQ Reporting Engine.

```csharp
public class ReportBuilderOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Obtient un ensemble non ordonné (c'est-à-dire une collection d'éléments uniques) contenantType objets dont les noms entièrement ou partiellement qualifiés peuvent être utilisés dans les modèles de rapport traités par cette instance engine pour appeler les membres statiques des types correspondants, effectuer des conversions de types, etc. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Obtient ou définit une valeur de chaîne affichée à la place d'une expression de modèle représentant une simple référence à un membre manquant d'un objet. La valeur par défaut est une chaîne vide. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Obtient ou définit un ensemble d'indicateurs contrôlant le comportement de ceci[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) instance lors de la création d'un rapport. |

## Exemples

Montre comment remplir un document avec des données.

```csharp
public void BuildReportData()
{
    // Il existe plusieurs façons de remplir un document avec des données :
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Voir également

* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
