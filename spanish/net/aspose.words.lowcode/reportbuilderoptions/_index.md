---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words LowCode ReportBuilderOptions, diseñada para mejorar su experiencia con el motor de informes LINQ con opciones personalizables para la generación de documentos sin problemas.
type: docs
weight: 4380
url: /es/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Representa opciones para la funcionalidad del motor de informes LINQ.

```csharp
public class ReportBuilderOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Obtiene un conjunto desordenado (es decir, una colección de elementos únicos) que contieneType objetos cuyos nombres total o parcialmente calificados se pueden usar dentro de las plantillas de informes procesadas por esta instancia de engine para invocar los miembros estáticos de los tipos correspondientes, realizar conversiones de tipos, etc. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Obtiene o establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Obtiene o establece un conjunto de indicadores que controlan el comportamiento de este[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) instancia al crear un informe. |

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

* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
