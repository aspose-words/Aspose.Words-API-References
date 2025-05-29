---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Options ReportingEngine pour personnaliser facilement les comportements de création de rapports avec des indicateurs flexibles pour des performances et un contrôle optimaux.
type: docs
weight: 40
url: /fr/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Obtient ou définit un ensemble d'indicateurs contrôlant le comportement de ceci[`ReportingEngine`](../) instance lors de la création d'un rapport.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Exemples

Montre comment autoriser les membres manquants.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Voir également

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
