---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words für .NET
description: Entdecken Sie die ReportBuilderOptions-Eigenschaft, um das Verhalten Ihrer ReportingEngine anzupassen und die Berichterstellung durch flexible Steuerung und verbesserte Funktionalität zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

Ruft eine Reihe von Flags ab oder setzt diese, die das Verhalten dieses[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) Instanz beim Erstellen eines Berichts.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument mit Daten gefüllt wird.

```csharp
public void BuildReportData()
{
    // Es gibt mehrere Möglichkeiten, ein Dokument mit Daten zu füllen:
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

### Siehe auch

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
