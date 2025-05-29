---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words para .NET
description: Descubra la propiedad Opciones de ReportingEngine para personalizar fácilmente los comportamientos de creación de informes con indicadores flexibles para lograr un rendimiento y control óptimos.
type: docs
weight: 40
url: /es/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Obtiene o establece un conjunto de indicadores que controlan el comportamiento de este[`ReportingEngine`](../) instancia al crear un informe.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Ejemplos

Muestra cómo permitir miembros faltantes.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Ver también

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
