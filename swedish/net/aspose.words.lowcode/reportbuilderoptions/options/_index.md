---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ReportBuilderOptions för att anpassa din ReportingEngines beteende, förbättra rapportskapandet med flexibel kontroll och förbättrad funktionalitet.
type: docs
weight: 40
url: /sv/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

Hämtar eller ställer in en uppsättning flaggor som styr beteendet hos detta[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) instans när du skapar en rapport.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Exempel

Visar hur man fyller dokumentet med data.

```csharp
public void BuildReportData()
{
    // Det finns flera sätt att fylla i dokument med data:
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

### Se även

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
