---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words para .NET
description: Desbloquee la potente automatización de documentos con Aspose.Words.ReportingEngine. Rellene fácilmente las plantillas con datos y personalice la configuración para generar informes sin interrupciones.
type: docs
weight: 5470
url: /es/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Proporciona rutinas para rellenar documentos de plantilla con datos y un conjunto de configuraciones para controlar estas rutinas.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) Artículo de documentación.

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
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Obtiene un conjunto desordenado (es decir, una colección de elementos únicos) que contieneType objetos cuyos nombres total o parcialmente calificados se pueden usar dentro de las plantillas de informes procesadas por esta instancia de engine para invocar los miembros estáticos de los tipos correspondientes, realizar conversiones de tipos, etc. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Obtiene o establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Obtiene o establece un conjunto de indicadores que controlan el comportamiento de este`ReportingEngine` instancia al crear un informe. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Obtiene o establece un valor que indica si las invocaciones de miembros de tipo personalizado realizadas mediante la API de reflexión están optimizadas mediante la generación dinámica de clases. El valor predeterminado es`verdadero` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Rellena el documento de plantilla especificado con datos de las fuentes especificadas, convirtiéndolo en un informe listo. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Devuelve tipos, cuyos miembros, así como los miembros de los tipos derivados, no deben ser accesibles para el motor a través de la sintaxis de plantilla. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Especifica los tipos, qué miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor a través de la sintaxis de plantilla. |

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
