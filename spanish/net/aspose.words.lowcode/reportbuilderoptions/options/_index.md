---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words para .NET
description: Descubra la propiedad ReportBuilderOptions para personalizar el comportamiento de su ReportingEngine, mejorando la creación de informes con un control flexible y una funcionalidad mejorada.
type: docs
weight: 40
url: /es/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

Obtiene o establece un conjunto de indicadores que controlan el comportamiento de este[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) instancia al crear un informe.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Ejemplos

Muestra cómo rellenar un documento con datos.

```csharp
public void BuildReportData()
{
    // Hay varias formas de rellenar un documento con datos:
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

### Ver también

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
