---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words LowCode ReportBuilderOptions-klassen, utformad för att förbättra din LINQ Reporting Engine-upplevelse med anpassningsbara alternativ för sömlös dokumentgenerering.
type: docs
weight: 4380
url: /sv/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Representerar alternativ för LINQ Reporting Engine-funktionen.

```csharp
public class ReportBuilderOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Hämtar en oordnad mängd (dvs. en samling unika objekt) som innehållerType objekt vars helt eller delvis kvalificerade namn kan användas inom rapportmallar som bearbetas av denna engine -instans för att anropa motsvarande typers statiska medlemmar, utföra typomvandlingar etc. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Hämtar eller ställer in ett strängvärde som skrivs ut istället för ett malluttryck som representerar en vanlig referens till en saknad medlem i ett objekt. Standardvärdet är en tom sträng. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Hämtar eller ställer in en uppsättning flaggor som styr beteendet hos detta[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) instans när du skapar en rapport. |

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

* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
