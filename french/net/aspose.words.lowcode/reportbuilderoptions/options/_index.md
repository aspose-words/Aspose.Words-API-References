---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ReportBuilderOptions pour personnaliser le comportement de votre ReportingEngine, améliorant la création de rapports avec un contrôle flexible et des fonctionnalités améliorées.
type: docs
weight: 40
url: /fr/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

Obtient ou définit un ensemble d'indicateurs contrôlant le comportement de ceci[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) instance lors de la création d'un rapport.

```csharp
public ReportBuildOptions Options { get; set; }
```

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

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
