---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words para .NET
description: Aspose.Words.Reporting.ReportingEngine clase. Proporciona rutinas para completar documentos de plantilla con datos y un conjunto de configuraciones para controlar estas rutinas en C#.
type: docs
weight: 4730
url: /es/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Proporciona rutinas para completar documentos de plantilla con datos y un conjunto de configuraciones para controlar estas rutinas.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) artículo de documentación.

```csharp
public class ReportingEngine
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Obtiene un conjunto desordenado (es decir, una colección de elementos únicos) que contieneTypeobjetos cuyos nombres total o parcialmente calificados se pueden usar dentro de las plantillas de informes procesadas por esta instancia de motor para invocar los miembros estáticos de los tipos correspondientes, realizar conversiones de tipos, etc. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Obtiene o establece un conjunto de indicadores que controlan el comportamiento de este`ReportingEngine` instancia mientras se crea un informe. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Obtiene o establece un valor que indica si las invocaciones de miembros de tipo personalizado realizadas a través de la API de reflexión están optimizadas mediante la generación dinámica de clases o no. El valor predeterminado es`verdadero` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Completa el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Completa el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Completa el documento de plantilla especificado con datos de las fuentes especificadas, convirtiéndolo en un informe listo. |
| [Equals](../../aspose.words.reporting/reportingengine/equals/)(*object*) | Determina si el objeto especificado tiene el mismo valor que el objeto actual. |
| [GetHashCode](../../aspose.words.reporting/reportingengine/gethashcode/)() | Sirve como función hash para este tipo. |

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
